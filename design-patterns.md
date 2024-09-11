# design-patterns
JavaScript(Vanilla/ES6/TypeScript) and Java  (GoF) design patterns

A design pattern is a general repeatable/reusable solution to a commonly occurring problem with a given context in software design. It can be treated as a description or template for how to solve a problem that can be used in many different situations.

## Creational

- Singleton
- Factory Method/Factory
- Abstract Factory
- Builder
- Prototype

## Structural

- Adapter
- Bridge
- Composite
- Decorator
- Flyweight
- Proxy
- Facade

## Behavioral

- Chain of Responsibility
- Command
- Interpreter
- Iterator
- Mediator
- Memento
- Observer
- State
- Strategy
- Template Method
- Visitor

## Backend communication design patterns
1. Request response
2. push
3. short polling
4. long polling
5. Server Sent Events
6. Publish Subscribe(Pub/Sub)
7. Multiplexing and Demultiplexing
8. Stateful and Stateless
9. Sidecart pattern


Sure! Here's a comprehensive overview of various design patterns with example code in Java, covering creational, structural, and behavioral patterns, as well as backend communication design patterns.

## **Creational Design Patterns**

### **1. Singleton**
Ensures a class has only one instance and provides a global point of access to it.

**Example:**

```java
public class Singleton {
    private static Singleton instance;

    private Singleton() {
        // private constructor to prevent instantiation
    }

    public static synchronized Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}
```

### **2. Factory Method**
Defines an interface for creating an object but lets subclasses alter the type of objects that will be created.

**Example:**

```java
// Product
interface Product {
    void use();
}

// Concrete Product
class ConcreteProductA implements Product {
    public void use() {
        System.out.println("Using Product A");
    }
}

class ConcreteProductB implements Product {
    public void use() {
        System.out.println("Using Product B");
    }
}

// Creator
abstract class Creator {
    public abstract Product factoryMethod();
    
    public void someOperation() {
        Product product = factoryMethod();
        product.use();
    }
}

// Concrete Creator
class ConcreteCreatorA extends Creator {
    public Product factoryMethod() {
        return new ConcreteProductA();
    }
}

class ConcreteCreatorB extends Creator {
    public Product factoryMethod() {
        return new ConcreteProductB();
    }
}
```

### **3. Abstract Factory**
Provides an interface for creating families of related or dependent objects without specifying their concrete classes.

**Example:**

```java
// Abstract Factory
interface AbstractFactory {
    Product createProduct();
}

// Concrete Factories
class ConcreteFactory1 implements AbstractFactory {
    public Product createProduct() {
        return new Product1();
    }
}

class ConcreteFactory2 implements AbstractFactory {
    public Product createProduct() {
        return new Product2();
    }
}

// Abstract Product
interface Product {
    void use();
}

// Concrete Products
class Product1 implements Product {
    public void use() {
        System.out.println("Using Product1");
    }
}

class Product2 implements Product {
    public void use() {
        System.out.println("Using Product2");
    }
}
```

### **4. Builder**
Separates the construction of a complex object from its representation so that the same construction process can create different representations.

**Example:**

```java
// Product
class Product {
    private String partA;
    private String partB;
    
    public void setPartA(String partA) {
        this.partA = partA;
    }
    
    public void setPartB(String partB) {
        this.partB = partB;
    }
    
    @Override
    public String toString() {
        return "Product with partA: " + partA + " and partB: " + partB;
    }
}

// Builder
abstract class Builder {
    protected Product product = new Product();
    
    public abstract void buildPartA();
    public abstract void buildPartB();
    
    public Product getResult() {
        return product;
    }
}

// Concrete Builder
class ConcreteBuilder extends Builder {
    public void buildPartA() {
        product.setPartA("Part A");
    }
    
    public void buildPartB() {
        product.setPartB("Part B");
    }
}

// Director
class Director {
    private Builder builder;
    
    public Director(Builder builder) {
        this.builder = builder;
    }
    
    public void construct() {
        builder.buildPartA();
        builder.buildPartB();
    }
}
```

### **5. Prototype**
Creates new objects by copying an existing object, known as the prototype.

**Example:**

```java
// Prototype
abstract class Prototype implements Cloneable {
    public abstract Prototype clone();
}

// Concrete Prototype
class ConcretePrototype extends Prototype {
    private String property;
    
    public ConcretePrototype(String property) {
        this.property = property;
    }
    
    public String getProperty() {
        return property;
    }
    
    public void setProperty(String property) {
        this.property = property;
    }
    
    @Override
    public ConcretePrototype clone() {
        try {
            return (ConcretePrototype) super.clone();
        } catch (CloneNotSupportedException e) {
            throw new RuntimeException(e);
        }
    }
}
```

## **Structural Design Patterns**

### **1. Adapter**
Allows incompatible interfaces to work together.

**Example:**

```java
// Target
interface Target {
    void request();
}

// Adaptee
class Adaptee {
    public void specificRequest() {
        System.out.println("Specific request");
    }
}

// Adapter
class Adapter implements Target {
    private Adaptee adaptee;
    
    public Adapter(Adaptee adaptee) {
        this.adaptee = adaptee;
    }
    
    public void request() {
        adaptee.specificRequest();
    }
}
```

### **2. Bridge**
Decouples an abstraction from its implementation so that the two can vary independently.

**Example:**

```java
// Abstraction
abstract class Abstraction {
    protected Implementor implementor;
    
    public Abstraction(Implementor implementor) {
        this.implementor = implementor;
    }
    
    public abstract void operation();
}

// Implementor
interface Implementor {
    void operationImpl();
}

// Concrete Implementor
class ConcreteImplementorA implements Implementor {
    public void operationImpl() {
        System.out.println("Concrete Implementor A");
    }
}

// Refined Abstraction
class RefinedAbstraction extends Abstraction {
    public RefinedAbstraction(Implementor implementor) {
        super(implementor);
    }
    
    public void operation() {
        implementor.operationImpl();
    }
}
```

### **3. Composite**
Allows you to compose objects into tree structures to represent part-whole hierarchies.

**Example:**

```java
// Component
interface Component {
    void operation();
}

// Leaf
class Leaf implements Component {
    public void operation() {
        System.out.println("Leaf operation");
    }
}

// Composite
class Composite implements Component {
    private List<Component> children = new ArrayList<>();
    
    public void add(Component component) {
        children.add(component);
    }
    
    public void operation() {
        for (Component component : children) {
            component.operation();
        }
    }
}
```

### **4. Decorator**
Adds additional responsibilities to an object dynamically.

**Example:**

```java
// Component
interface Component {
    void operation();
}

// Concrete Component
class ConcreteComponent implements Component {
    public void operation() {
        System.out.println("ConcreteComponent operation");
    }
}

// Decorator
abstract class Decorator implements Component {
    protected Component component;
    
    public Decorator(Component component) {
        this.component = component;
    }
    
    public void operation() {
        component.operation();
    }
}

// Concrete Decorator
class ConcreteDecorator extends Decorator {
    public ConcreteDecorator(Component component) {
        super(component);
    }
    
    public void operation() {
        super.operation();
        addedBehavior();
    }
    
    private void addedBehavior() {
        System.out.println("Added behavior");
    }
}
```

### **5. Flyweight**
Reduces the cost of creating and manipulating a large number of similar objects.

**Example:**

```java
// Flyweight
interface Flyweight {
    void operation();
}

// Concrete Flyweight
class ConcreteFlyweight implements Flyweight {
    private String intrinsicState;
    
    public ConcreteFlyweight(String state) {
        this.intrinsicState = state;
    }
    
    public void operation() {
        System.out.println("ConcreteFlyweight operation with state " + intrinsicState);
    }
}

// Flyweight Factory
class FlyweightFactory {
    private Map<String, Flyweight> flyweights = new HashMap<>();
    
    public Flyweight getFlyweight(String state) {
        if (!flyweights.containsKey(state)) {
            flyweights.put(state, new ConcreteFlyweight(state));
        }
        return flyweights.get(state);
    }
}
```

### **6. Proxy**
Provides a surrogate or placeholder for another object to control access to it.

**Example:**

```java
// Subject
interface Subject {
    void request();
}

// RealSubject
class RealSubject implements Subject {
    public void request() {
        System.out.println("RealSubject request");
    }
}

// Proxy
class Proxy implements Subject {
    private RealSubject realSubject;
    
    public void request() {
        if (realSubject == null) {
            realSubject = new RealSubject();
        }
        realSubject.request();
    }
}
```

### **7. Facade**
Provides a simplified interface to a complex subsystem.

**Example:**

```java
// Subsystem classes
class Subsystem1 {
    public void operation1() {
        System.out.println("Subsystem1 operation1");
    }
}

class Subsystem2 {
    public void operation2() {
        System.out.println("Subsystem2 operation2");
    }
}

// Facade
class Facade {
    private Subsystem1 subsystem1 = new Subsystem1();
    private Subsystem2 subsystem2 = new Subsystem2();
    
    public void simplifiedOperation() {
        subsystem1.operation1();
        subsystem2.operation2();
    }
}
```

## **Behavioral Design Patterns**

### **1. Chain of Responsibility**
Passes a request along a chain of handlers, where each handler decides whether to process the request or pass it along the chain.

**Example:**

```java
// Handler
abstract class Handler {
    protected Handler successor;
    
    public void setSuccessor(Handler successor) {
        this.successor = successor;
    }
    
    public abstract void handleRequest(int request);
}

// Concrete Handler
class ConcreteHandlerA extends Handler {
    public void handleRequest(int request)

 {
        if (request < 10) {
            System.out.println("Handler A handled request " + request);
        } else if (successor != null) {
            successor.handleRequest(request);
        }
    }
}

class ConcreteHandlerB extends Handler {
    public void handleRequest(int request) {
        if (request >= 10 && request < 20) {
            System.out.println("Handler B handled request " + request);
        } else if (successor != null) {
            successor.handleRequest(request);
        }
    }
}
```

### **2. Command**
Encapsulates a request as an object, thereby allowing for parameterization of clients with queues, requests, and operations.

**Example:**

```java
// Command
interface Command {
    void execute();
}

// Concrete Command
class LightOnCommand implements Command {
    private Light light;
    
    public LightOnCommand(Light light) {
        this.light = light;
    }
    
    public void execute() {
        light.turnOn();
    }
}

// Receiver
class Light {
    public void turnOn() {
        System.out.println("Light is on");
    }
}

// Invoker
class RemoteControl {
    private Command command;
    
    public void setCommand(Command command) {
        this.command = command;
    }
    
    public void pressButton() {
        command.execute();
    }
}
```

### **3. Interpreter**
Defines a grammar for interpreting sentences in a language and provides an interpreter to interpret the sentences.

**Example:**

```java
// Abstract Expression
interface Expression {
    boolean interpret(String context);
}

// Terminal Expression
class TerminalExpression implements Expression {
    private String data;
    
    public TerminalExpression(String data) {
        this.data = data;
    }
    
    public boolean interpret(String context) {
        return context.contains(data);
    }
}

// Context
class Context {
    private Expression expression;
    
    public Context(Expression expression) {
        this.expression = expression;
    }
    
    public boolean interpret(String context) {
        return expression.interpret(context);
    }
}
```

### **4. Iterator**
Provides a way to access the elements of an aggregate object sequentially without exposing its underlying representation.

**Example:**

```java
// Iterator
interface Iterator {
    boolean hasNext();
    Object next();
}

// Aggregate
interface IterableCollection {
    Iterator createIterator();
}

// Concrete Iterator
class ConcreteIterator implements Iterator {
    private List<Object> items;
    private int position = 0;
    
    public ConcreteIterator(List<Object> items) {
        this.items = items;
    }
    
    public boolean hasNext() {
        return position < items.size();
    }
    
    public Object next() {
        return items.get(position++);
    }
}

// Concrete Aggregate
class ConcreteCollection implements IterableCollection {
    private List<Object> items = new ArrayList<>();
    
    public void addItem(Object item) {
        items.add(item);
    }
    
    public Iterator createIterator() {
        return new ConcreteIterator(items);
    }
}
```

### **5. Mediator**
Defines an object that encapsulates how a set of objects interact and promotes loose coupling.

**Example:**

```java
// Mediator
interface Mediator {
    void send(String message, Colleague colleague);
}

// Concrete Mediator
class ConcreteMediator implements Mediator {
    private ConcreteColleague1 colleague1;
    private ConcreteColleague2 colleague2;
    
    public void setColleague1(ConcreteColleague1 colleague1) {
        this.colleague1 = colleague1;
    }
    
    public void setColleague2(ConcreteColleague2 colleague2) {
        this.colleague2 = colleague2;
    }
    
    public void send(String message, Colleague colleague) {
        if (colleague == colleague1) {
            colleague2.receive(message);
        } else {
            colleague1.receive(message);
        }
    }
}

// Colleague
abstract class Colleague {
    protected Mediator mediator;
    
    public Colleague(Mediator mediator) {
        this.mediator = mediator;
    }
    
    public abstract void receive(String message);
}

// Concrete Colleagues
class ConcreteColleague1 extends Colleague {
    public ConcreteColleague1(Mediator mediator) {
        super(mediator);
    }
    
    public void receive(String message) {
        System.out.println("Colleague1 received: " + message);
    }
}

class ConcreteColleague2 extends Colleague {
    public ConcreteColleague2(Mediator mediator) {
        super(mediator);
    }
    
    public void receive(String message) {
        System.out.println("Colleague2 received: " + message);
    }
}
```

### **6. Memento**
Captures and restores an object's internal state without violating encapsulation.

**Example:**

```java
// Memento
class Memento {
    private String state;
    
    public Memento(String state) {
        this.state = state;
    }
    
    public String getState() {
        return state;
    }
}

// Originator
class Originator {
    private String state;
    
    public void setState(String state) {
        this.state = state;
    }
    
    public String getState() {
        return state;
    }
    
    public Memento saveStateToMemento() {
        return new Memento(state);
    }
    
    public void getStateFromMemento(Memento memento) {
        state = memento.getState();
    }
}

// Caretaker
class Caretaker {
    private Memento memento;
    
    public void saveMemento(Memento memento) {
        this.memento = memento;
    }
    
    public Memento getMemento() {
        return memento;
    }
}
```

### **7. Observer**
Defines a dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.

**Example:**

```java
// Observer
interface Observer {
    void update(String message);
}

// Subject
interface Subject {
    void addObserver(Observer observer);
    void removeObserver(Observer observer);
    void notifyObservers();
}

// Concrete Subject
class ConcreteSubject implements Subject {
    private List<Observer> observers = new ArrayList<>();
    private String state;
    
    public void setState(String state) {
        this.state = state;
        notifyObservers();
    }
    
    public String getState() {
        return state;
    }
    
    public void addObserver(Observer observer) {
        observers.add(observer);
    }
    
    public void removeObserver(Observer observer) {
        observers.remove(observer);
    }
    
    public void notifyObservers() {
        for (Observer observer : observers) {
            observer.update(state);
        }
    }
}

// Concrete Observer
class ConcreteObserver implements Observer {
    private String name;
    
    public ConcreteObserver(String name) {
        this.name = name;
    }
    
    public void update(String message) {
        System.out.println(name + " received update: " + message);
    }
}
```

### **8. State**
Allows an object to alter its behavior when its internal state changes.

**Example:**

```java
// State
interface State {
    void handleRequest();
}

// Concrete States
class ConcreteStateA implements State {
    public void handleRequest() {
        System.out.println("Handling request in State A");
    }
}

class ConcreteStateB implements State {
    public void handleRequest() {
        System.out.println("Handling request in State B");
    }
}

// Context
class Context {
    private State state;
    
    public void setState(State state) {
        this.state = state;
    }
    
    public void request() {
        state.handleRequest();
    }
}
```

### **9. Strategy**
Defines a family of algorithms, encapsulates each one, and makes them interchangeable.

**Example:**

```java
// Strategy
interface Strategy {
    void execute();
}

// Concrete Strategies
class ConcreteStrategyA implements Strategy {
    public void execute() {
        System.out.println("Executing Strategy A");
    }
}

class ConcreteStrategyB implements Strategy {
    public void execute() {
        System.out.println("Executing Strategy B");
    }
}

// Context
class Context {
    private Strategy strategy;
    
    public void setStrategy(Strategy strategy) {
        this.strategy = strategy;
    }
    
    public void executeStrategy() {
        strategy.execute();
    }
}
```

### **10. Template Method**
Defines the skeleton of an algorithm in the superclass but lets subclasses redefine certain steps of the algorithm without changing its structure.

**Example:**

```java
// Abstract Class
abstract class AbstractClass {
    public final void templateMethod() {
        step1();
        step2();
        step3();
    }
    
    protected abstract void step1();
    protected abstract void step2();
    
    private void step3() {
        System.out.println("Step 3");
    }
}

// Concrete Class
class ConcreteClass extends AbstractClass {
    protected void step1() {
        System.out.println("ConcreteClass step1");
    }
    
    protected void step2() {
        System.out.println("ConcreteClass step2");
    }
}
```

### **11. Visitor**
Defines a new operation to a group of objects without changing the classes of the elements on which it operates.

**Example:**

```java
// Visitor
interface Visitor {
    void visit(ElementA elementA);
    void visit(ElementB elementB);
}

// Concrete Visitors
class ConcreteVisitor1 implements Visitor {
    public void visit(ElementA elementA) {
        System.out.println("ConcreteVisitor1 visiting ElementA");
    }
    
    public void visit(ElementB elementB) {
        System.out.println("ConcreteVisitor1 visiting ElementB");
    }
}

class ConcreteVisitor2 implements Visitor {
    public void visit(ElementA elementA) {
        System.out.println("ConcreteVisitor2 visiting ElementA");
    }
    
    public void visit(ElementB elementB) {
        System.out.println("ConcreteVisitor2 visiting ElementB");
    }
}

// Element
interface Element {
   

 void accept(Visitor visitor);
}

// Concrete Elements
class ElementA implements Element {
    public void accept(Visitor visitor) {
        visitor.visit(this);
    }
}

class ElementB implements Element {
    public void accept(Visitor visitor) {
        visitor.visit(this);
    }
}
```

## **Backend Communication Design Patterns**

### **1. Request Response**
A pattern where a client sends a request to a server and waits for a response.

**Example:**

```java
// Client
public class Client {
    public static void main(String[] args) {
        try (Socket socket = new Socket("localhost", 8080);
             PrintWriter out = new PrintWriter(socket.getOutputStream(), true);
             BufferedReader in = new BufferedReader(new InputStreamReader(socket.getInputStream()))) {

            out.println("Hello Server");
            String response = in.readLine();
            System.out.println("Server response: " + response);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### **2. Push**
The server sends updates to the client whenever new data is available.

**Example:**

```java
// Server (using WebSocket for push communication)
@ServerEndpoint("/push")
public class PushServer {
    @OnMessage
    public void onMessage(Session session, String message) {
        // Send a message to the client
        session.getAsyncRemote().sendText("Server response to: " + message);
    }
}

// Client (using WebSocket)
WebSocket ws = new WebSocket("ws://localhost:8080/push");
ws.onmessage = function(event) {
    console.log("Received message: " + event.data);
};
ws.send("Hello Server");
```

### **3. Short Polling**
The client repeatedly polls the server at regular intervals to check for new data.

**Example:**

```java
// Client
public class ShortPollingClient {
    public static void main(String[] args) {
        while (true) {
            try {
                URL url = new URL("http://localhost:8080/check");
                HttpURLConnection conn = (HttpURLConnection) url.openConnection();
                conn.setRequestMethod("GET");
                
                BufferedReader in = new BufferedReader(new InputStreamReader(conn.getInputStream()));
                String response = in.readLine();
                System.out.println("Server response: " + response);
                in.close();
                
                Thread.sleep(5000); // wait for 5 seconds
            } catch (IOException | InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}
```

### **4. Long Polling**
A client requests information from the server and keeps the connection open until the server has new information.

**Example:**

```java
// Server (using Servlet)
@WebServlet("/longpolling")
public class LongPollingServlet extends HttpServlet {
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws IOException {
        // Simulate long wait for new data
        try {
            Thread.sleep(10000); // wait for 10 seconds
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        
        response.getWriter().write("New data available");
    }
}

// Client
public class LongPollingClient {
    public static void main(String[] args) {
        while (true) {
            try {
                URL url = new URL("http://localhost:8080/longpolling");
                HttpURLConnection conn = (HttpURLConnection) url.openConnection();
                conn.setRequestMethod("GET");
                
                BufferedReader in = new BufferedReader(new InputStreamReader(conn.getInputStream()));
                String response = in.readLine();
                System.out.println("Server response: " + response);
                in.close();
                
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }
}
```

### **5. Server-Sent Events (SSE)**
A server pushes updates to the client over a single, long-lived HTTP connection.

**Example:**

```java
// Server (using SSE)
@ServerEndpoint("/events")
public class SSEServer {
    @OnOpen
    public void onOpen(Session session) {
        // Send periodic updates
        new Thread(() -> {
            try {
                while (true) {
                    session.getBasicRemote().sendText("Update at " + new Date());
                    Thread.sleep(5000); // wait for 5 seconds
                }
            } catch (IOException | InterruptedException e) {
                e.printStackTrace();
            }
        }).start();
    }
}

// Client (JavaScript example)
const eventSource = new EventSource("http://localhost:8080/events");
eventSource.onmessage = function(event) {
    console.log("Received event: " + event.data);
};
```

### **6. Publish-Subscribe (Pub/Sub)**
A messaging pattern where publishers send messages to a topic, and subscribers receive messages from that topic.

**Example:**

```java
// Publisher
public class Publisher {
    private MessageBroker broker;
    
    public Publisher(MessageBroker broker) {
        this.broker = broker;
    }
    
    public void publish(String message) {
        broker.publish(message);
    }
}

// Subscriber
public class Subscriber {
    private MessageBroker broker;
    
    public Subscriber(MessageBroker broker) {
        this.broker = broker;
        broker.subscribe(this::receiveMessage);
    }
    
    public void receiveMessage(String message) {
        System.out.println("Received message: " + message);
    }
}

// MessageBroker
public class MessageBroker {
    private List<Consumer<String>> subscribers = new ArrayList<>();
    
    public void subscribe(Consumer<String> subscriber) {
        subscribers.add(subscriber);
    }
    
    public void publish(String message) {
        for (Consumer<String> subscriber : subscribers) {
            subscriber.accept(message);
        }
    }
}
```

### **7. Multiplexing and Demultiplexing**
A technique for sending multiple signals or data streams over a single channel and then separating them at the receiving end.

**Example:**

```java
// Multiplexer
class Multiplexer {
    private List<Channel> channels = new ArrayList<>();
    
    public void addChannel(Channel channel) {
        channels.add(channel);
    }
    
    public void send(String message) {
        for (Channel channel : channels) {
            channel.send(message);
        }
    }
}

// Channel
interface Channel {
    void send(String message);
}

// Demultiplexer (receiving end)
class Demultiplexer {
    public void receive(String message) {
        System.out.println("Received message: " + message);
    }
}
```

### **8. Stateful and Stateless**
- **Stateful**: Maintains the state of interactions between client and server.
- **Stateless**: Each request from a client to a server must contain all the information the server needs to fulfill that request.

**Example:**

```java
// Stateless Example
// StatelessServlet
@WebServlet("/stateless")
public class StatelessServlet extends HttpServlet {
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws IOException {
        response.getWriter().write("Stateless response");
    }
}

// Stateful Example
// StatefulServlet
@WebServlet("/stateful")
public class StatefulServlet extends HttpServlet {
    private Map<String, String> state = new HashMap<>();
    
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws IOException {
        String id = request.getParameter("id");
        String value = state.getOrDefault(id, "Default value");
        response.getWriter().write("Stateful response: " + value);
    }
    
    protected void doPost(HttpServletRequest request, HttpServletResponse response) throws IOException {
        String id = request.getParameter("id");
        String value = request.getParameter("value");
        state.put(id, value);
        response.getWriter().write("State updated");
    }
}
```

### **9. Sidecar Pattern**
A pattern where a secondary service (sidecar) runs alongside the primary service to provide auxiliary capabilities.

**Example:**

```java
// Main Application
public class MainApp {
    public static void main(String[] args) {
        // Start primary service
        System.out.println("Primary service running");
        
        // Start sidecar service (e.g., monitoring)
        new SidecarService().start();
    }
}

// Sidecar Service
class SidecarService {
    public void start() {
        System.out.println("Sidecar service running");
    }
}
```

These examples should give you a solid understanding of various design patterns and backend communication techniques, including their implementation in Java.
