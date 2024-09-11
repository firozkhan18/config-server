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


Sure! Here’s an in-depth explanation of the design patterns, their concepts, examples, and real-time use cases.

---

## Creational Design Patterns

**1. Singleton**

**Concept:** Ensures that a class has only one instance and provides a global point of access to it.

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

**Real-Time Use Case:** Database connection pool management where a single instance controls access to the database to avoid multiple connections and ensure consistency.

---

**2. Factory Method/Factory**

**Concept:** Defines an interface for creating an object but lets subclasses alter the type of objects that will be created.

**Example:**

```java
// Product Interface
interface Product {
    void create();
}

// Concrete Product
class ConcreteProductA implements Product {
    public void create() {
        System.out.println("Product A created");
    }
}

// Creator
abstract class Creator {
    public abstract Product factoryMethod();
    
    public void anOperation() {
        Product product = factoryMethod();
        product.create();
    }
}

// Concrete Creator
class ConcreteCreatorA extends Creator {
    public Product factoryMethod() {
        return new ConcreteProductA();
    }
}
```

**Real-Time Use Case:** GUI libraries where different operating systems require different implementations of UI components.

---

**3. Abstract Factory**

**Concept:** Provides an interface for creating families of related or dependent objects without specifying their concrete classes.

**Example:**

```java
// Abstract Factory
interface AbstractFactory {
    ProductA createProductA();
    ProductB createProductB();
}

// Concrete Factory
class ConcreteFactory1 implements AbstractFactory {
    public ProductA createProductA() {
        return new ConcreteProductA1();
    }
    
    public ProductB createProductB() {
        return new ConcreteProductB1();
    }
}

// Abstract Products
interface ProductA {}
interface ProductB {}

// Concrete Products
class ConcreteProductA1 implements ProductA {}
class ConcreteProductB1 implements ProductB {}
```

**Real-Time Use Case:** Cross-platform software where different factories are used to create different UI elements suitable for each platform.

---

**4. Builder**

**Concept:** Separates the construction of a complex object from its representation, allowing the same construction process to create different representations.

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
}

// Builder
abstract class Builder {
    public abstract void buildPartA();
    public abstract void buildPartB();
    public abstract Product getResult();
}

// Concrete Builder
class ConcreteBuilder extends Builder {
    private Product product = new Product();
    
    public void buildPartA() {
        product.setPartA("PartA");
    }
    
    public void buildPartB() {
        product.setPartB("PartB");
    }
    
    public Product getResult() {
        return product;
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

**Real-Time Use Case:** Constructing complex documents like XML or JSON configurations where different components and settings need to be assembled.

---

**5. Prototype**

**Concept:** Creates new objects by copying an existing object, known as the prototype.

**Example:**

```java
// Prototype
abstract class Prototype implements Cloneable {
    public abstract Prototype clone();
}

// Concrete Prototype
class ConcretePrototype extends Prototype {
    private String field;
    
    public ConcretePrototype(String field) {
        this.field = field;
    }
    
    public Prototype clone() {
        return new ConcretePrototype(this.field);
    }
}
```

**Real-Time Use Case:** When creating multiple instances of a class with similar configurations, like GUI elements in an application where each can be cloned from a prototype.

---

## Structural Design Patterns

**1. Adapter**

**Concept:** Converts the interface of a class into another interface clients expect.

**Example:**

```java
// Target Interface
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

**Real-Time Use Case:** Integrating a new system with an existing legacy system where the interfaces are incompatible.

---

**2. Bridge**

**Concept:** Decouples an abstraction from its implementation so that the two can vary independently.

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
class ConcreteImplementor implements Implementor {
    public void operationImpl() {
        System.out.println("Operation Implemented");
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

**Real-Time Use Case:** Designing a graphical user interface where the abstraction (e.g., a window) can be implemented in different ways (e.g., using different platforms).

---

**3. Composite**

**Concept:** Allows individual objects and compositions of objects to be treated uniformly.

**Example:**

```java
// Component
abstract class Component {
    public abstract void operation();
}

// Leaf
class Leaf extends Component {
    public void operation() {
        System.out.println("Leaf operation");
    }
}

// Composite
class Composite extends Component {
    private List<Component> children = new ArrayList<>();
    
    public void add(Component component) {
        children.add(component);
    }
    
    public void operation() {
        for (Component child : children) {
            child.operation();
        }
    }
}
```

**Real-Time Use Case:** Representing hierarchical structures like files and directories where operations can be performed on both individual files and directories.

---

**4. Decorator**

**Concept:** Adds additional responsibilities to an object dynamically.

**Example:**

```java
// Component
interface Component {
    void operation();
}

// Concrete Component
class ConcreteComponent implements Component {
    public void operation() {
        System.out.println("Concrete Component");
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
        System.out.println("Concrete Decorator");
    }
}
```

**Real-Time Use Case:** Adding features to a user interface component dynamically, such as adding borders, scrollbars, or shadows to a window.

---

**5. Flyweight**

**Concept:** Reduces the cost of creating and manipulating a large number of similar objects by sharing common parts of the state.

**Example:**

```java
// Flyweight
interface Flyweight {
    void operation(String extrinsicState);
}

// Concrete Flyweight
class ConcreteFlyweight implements Flyweight {
    private String intrinsicState;
    
    public ConcreteFlyweight(String intrinsicState) {
        this.intrinsicState = intrinsicState;
    }
    
    public void operation(String extrinsicState) {
        System.out.println("Intrinsic State: " + intrinsicState + ", Extrinsic State: " + extrinsicState);
    }
}

// Flyweight Factory
class FlyweightFactory {
    private Map<String, Flyweight> flyweights = new HashMap<>();
    
    public Flyweight getFlyweight(String key) {
        Flyweight flyweight = flyweights.get(key);
        if (flyweight == null) {
            flyweight = new ConcreteFlyweight(key);
            flyweights.put(key, flyweight);
        }
        return flyweight;
    }
}
```

**Real-Time Use Case:** Rendering text in a graphical application where the same font style and size are used across multiple pieces of text.

---

**6. Proxy**

**Concept:** Provides a surrogate or placeholder for another object to control access to it.

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

**Real-Time Use Case:** Implementing access control for a resource-intensive object like a network connection or file system.

---

**7. Facade**

**Concept:** Provides a unified interface to a set of interfaces in a subsystem, making it easier to use.

**Example:**

```java
// Subsystem Classes
class SubsystemA {
    public void operationA() {
        System.out.println("Subsystem A operation");
   

 }
}

class SubsystemB {
    public void operationB() {
        System.out.println("Subsystem B operation");
    }
}

// Facade
class Facade {
    private SubsystemA subsystemA = new SubsystemA();
    private SubsystemB subsystemB = new SubsystemB();
    
    public void performOperations() {
        subsystemA.operationA();
        subsystemB.operationB();
    }
}
```

**Real-Time Use Case:** Simplifying interactions with a complex library or system by providing a simpler API.

---

## Behavioral Design Patterns

**1. Chain of Responsibility**

**Concept:** Passes a request along a chain of handlers, where each handler can either handle the request or pass it to the next handler.

**Example:**

```java
// Handler
abstract class Handler {
    private Handler next;
    
    public void setNext(Handler next) {
        this.next = next;
    }
    
    public abstract void handleRequest(int request);
    
    protected void passToNext(int request) {
        if (next != null) {
            next.handleRequest(request);
        }
    }
}

// Concrete Handlers
class ConcreteHandlerA extends Handler {
    public void handleRequest(int request) {
        if (request < 10) {
            System.out.println("Handler A handled request " + request);
        } else {
            passToNext(request);
        }
    }
}

class ConcreteHandlerB extends Handler {
    public void handleRequest(int request) {
        if (request < 20) {
            System.out.println("Handler B handled request " + request);
        } else {
            passToNext(request);
        }
    }
}
```

**Real-Time Use Case:** Handling HTTP requests in a web server where each handler processes the request or passes it to the next handler in the chain.

---

**2. Command**

**Concept:** Encapsulates a request as an object, thereby allowing for parameterization of clients with different requests, queuing of requests, and logging of the requests.

**Example:**

```java
// Command Interface
interface Command {
    void execute();
}

// Concrete Commands
class ConcreteCommandA implements Command {
    public void execute() {
        System.out.println("Executing Command A");
    }
}

class ConcreteCommandB implements Command {
    public void execute() {
        System.out.println("Executing Command B");
    }
}

// Invoker
class Invoker {
    private Command command;
    
    public void setCommand(Command command) {
        this.command = command;
    }
    
    public void invoke() {
        command.execute();
    }
}
```

**Real-Time Use Case:** Implementing undo/redo functionality in applications where commands are stored and can be executed or reverted.

---

**3. Interpreter**

**Concept:** Defines a grammatical representation for a language and provides an interpreter to interpret the sentences of the language.

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
    
    public boolean execute(String context) {
        return expression.interpret(context);
    }
}
```

**Real-Time Use Case:** Implementing a simple language interpreter for query processing where different expressions are evaluated based on context.

---

**4. Iterator**

**Concept:** Provides a way to access the elements of an aggregate object sequentially without exposing its underlying representation.

**Example:**

```java
// Iterator Interface
interface Iterator<T> {
    boolean hasNext();
    T next();
}

// Aggregate Interface
interface IterableCollection<T> {
    Iterator<T> createIterator();
}

// Concrete Collection
class ConcreteCollection implements IterableCollection<String> {
    private List<String> items = new ArrayList<>();
    
    public void add(String item) {
        items.add(item);
    }
    
    public Iterator<String> createIterator() {
        return new ConcreteIterator(items);
    }
}

// Concrete Iterator
class ConcreteIterator implements Iterator<String> {
    private List<String> items;
    private int position;
    
    public ConcreteIterator(List<String> items) {
        this.items = items;
    }
    
    public boolean hasNext() {
        return position < items.size();
    }
    
    public String next() {
        return items.get(position++);
    }
}
```

**Real-Time Use Case:** Iterating over collections in data structures like lists or arrays where the internal structure is hidden.

---

**5. Mediator**

**Concept:** Defines an object that encapsulates how a set of objects interact, promoting loose coupling by keeping objects from referring to each other explicitly.

**Example:**

```java
// Mediator Interface
interface Mediator {
    void notify(Object sender, String event);
}

// Concrete Mediator
class ConcreteMediator implements Mediator {
    private ColleagueA colleagueA;
    private ColleagueB colleagueB;
    
    public void setColleagueA(ColleagueA colleagueA) {
        this.colleagueA = colleagueA;
    }
    
    public void setColleagueB(ColleagueB colleagueB) {
        this.colleagueB = colleagueB;
    }
    
    public void notify(Object sender, String event) {
        if (sender == colleagueA) {
            colleagueB.doAction();
        } else if (sender == colleagueB) {
            colleagueA.doAction();
        }
    }
}

// Colleague Classes
class ColleagueA {
    private Mediator mediator;
    
    public ColleagueA(Mediator mediator) {
        this.mediator = mediator;
    }
    
    public void doAction() {
        System.out.println("ColleagueA does action");
        mediator.notify(this, "action");
    }
}

class ColleagueB {
    private Mediator mediator;
    
    public ColleagueB(Mediator mediator) {
        this.mediator = mediator;
    }
    
    public void doAction() {
        System.out.println("ColleagueB does action");
        mediator.notify(this, "action");
    }
}
```

**Real-Time Use Case:** Implementing a chat application where the mediator handles message exchanges between different users.

---

**6. Memento**

**Concept:** Captures and externalizes an object’s internal state without violating encapsulation so that the object can be restored to that state later.

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
    
    public void saveState(Originator originator) {
        memento = originator.saveStateToMemento();
    }
    
    public void restoreState(Originator originator) {
        originator.getStateFromMemento(memento);
    }
}
```

**Real-Time Use Case:** Implementing undo functionality in applications where the state of an object can be restored to a previous version.

---

**7. Observer**

**Concept:** Defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.

**Example:**

```java
// Subject
interface Subject {
    void addObserver(Observer observer);
    void removeObserver(Observer observer);
    void notifyObservers();
}

// Concrete Subject
class ConcreteSubject implements Subject {
    private List<Observer> observers = new ArrayList<>();
    
    public void addObserver(Observer observer) {
        observers.add(observer);
    }
    
    public void removeObserver(Observer observer) {
        observers.remove(observer);
    }
    
    public void notifyObservers() {
        for (Observer observer : observers) {
            observer.update();
        }
    }
}

// Observer Interface
interface Observer {
    void update();
}

// Concrete Observer
class ConcreteObserver implements Observer {
    public void update() {
        System.out.println("Observer updated");
    }
}
```

**Real-Time Use Case:** Implementing a stock market system where subscribers receive updates whenever stock prices change.

---

**8. State**

**Concept:** Allows an object to alter its behavior when its internal state changes. The object will appear to change its class.

**Example:**

```java
// State Interface
interface State {
    void handle();
}

// Concrete States
class ConcreteStateA implements State {
    public void handle() {
        System.out.println("Handling state A");
    }
}

class ConcreteStateB implements State {
    public void handle() {
        System.out.println("Handling state B");
    }
}

// Context
class Context {
    private State state;
    
    public void setState(State state) {
        this.state = state;
    }
    
    public void request() {
        state.handle();
    }
}
```

**Real-Time Use Case:** Implementing a traffic light system where the behavior changes based on the light’s current state (e.g., red, green, yellow).

---

**9. Strategy**

**Concept:** Defines a family of algorithms, encapsulates each one, and makes them interchangeable. The strategy lets the algorithm vary independently from clients that use it.

**Example:**

```java
// Strategy Interface
interface Strategy {
    void execute();
}

// Concrete Strategies
class ConcreteStrategyA implements Strategy {
    public void execute() {
        System.out.println("Strategy A executed");
    }
}

class ConcreteStrategyB implements Strategy {
    public void execute() {
        System.out

.println("Strategy B executed");
    }
}

// Context
class Context {
    private Strategy strategy;
    
    public void setStrategy(Strategy strategy) {
        this.strategy = strategy;
    }
    
    public void performAction() {
        strategy.execute();
    }
}
```

**Real-Time Use Case:** Implementing different payment methods in an e-commerce application where users can choose between credit card, PayPal, or cryptocurrency.

---

**10. Template Method**

**Concept:** Defines the skeleton of an algorithm in a base class but lets subclasses override specific steps of the algorithm without changing its structure.

**Example:**

```java
// Abstract Class
abstract class AbstractClass {
    public void templateMethod() {
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
        System.out.println("Step 1");
    }
    
    protected void step2() {
        System.out.println("Step 2");
    }
}
```

**Real-Time Use Case:** Implementing a framework for file processing where common steps (e.g., opening and closing files) are defined in the template method, and specific processing is handled by subclasses.

---

**11. Visitor**

**Concept:** Defines a new operation to a group of objects without changing the objects themselves. The visitor pattern separates algorithms from the objects on which they operate.

**Example:**

```java
// Visitor Interface
interface Visitor {
    void visit(Element element);
}

// Concrete Visitor
class ConcreteVisitor implements Visitor {
    public void visit(Element element) {
        System.out.println("Visiting " + element);
    }
}

// Element Interface
interface Element {
    void accept(Visitor visitor);
}

// Concrete Element
class ConcreteElement implements Element {
    public void accept(Visitor visitor) {
        visitor.visit(this);
    }
}
```

**Real-Time Use Case:** Adding new operations to a data structure (like a document with various elements) without modifying the structure or its elements.

---

## Backend Communication Design Patterns

**1. Request Response**

**Concept:** A client sends a request to a server, and the server responds with a result. This is the most common pattern in client-server communication.

**Example:** HTTP requests and responses where a client requests data from a server, and the server responds with the requested data.

**Real-Time Use Case:** Web browsing where the browser requests web pages and the server responds with HTML content.

---

**2. Push**

**Concept:** The server sends data to the client without the client explicitly requesting it.

**Example:** WebSocket connections where the server can push updates to the client in real-time.

**Real-Time Use Case:** Real-time chat applications where new messages are pushed to clients as they arrive.

---

**3. Short Polling**

**Concept:** The client periodically sends requests to the server to check for updates.

**Example:** A client sends a request every few seconds to check if new data is available.

**Real-Time Use Case:** Live sports score updates where the client polls the server periodically to fetch the latest scores.

---

**4. Long Polling**

**Concept:** The client sends a request to the server, and the server holds the request open until new data is available or a timeout occurs.

**Example:** The server holds the request until it has new data, then sends the data and closes the connection.

**Real-Time Use Case:** Notification systems where the client waits for server updates and receives notifications as they become available.

---

**5. Server-Sent Events (SSE)**

**Concept:** The server sends updates to the client over a single, long-lived HTTP connection.

**Example:** A continuous stream of updates sent from the server to the client using `EventSource` API in JavaScript.

**Real-Time Use Case:** Real-time dashboards that receive live updates from the server, such as financial data feeds or live traffic reports.

---

**6. Publish-Subscribe (Pub/Sub)**

**Concept:** A messaging pattern where publishers send messages to a topic and subscribers receive messages from that topic.

**Example:** Message brokers like Apache Kafka or RabbitMQ where messages are published to topics and consumers subscribe to those topics.

**Real-Time Use Case:** Event-driven systems where different components subscribe to events and react to them as they occur.

---

**7. Multiplexing and Demultiplexing**

**Concept:** Multiplexing involves combining multiple data streams into one, while demultiplexing involves separating them back out.

**Example:** HTTP/2 multiplexing where multiple HTTP requests and responses are sent over a single connection.

**Real-Time Use Case:** Streaming video services where multiple video streams are sent over a single connection to optimize bandwidth usage.

---

**8. Stateful and Stateless**

**Concept:** Stateful systems maintain client state across requests, while stateless systems do not.

**Example:** Stateful: A session-based web application where user data is stored between requests. Stateless: REST APIs where each request is independent and carries all necessary information.

**Real-Time Use Case:** E-commerce applications (stateful) where user sessions and shopping carts are maintained, versus RESTful services (stateless) where each request is independent.

---

**9. Sidecar Pattern**

**Concept:** Deploys a secondary component (sidecar) alongside a primary application to provide additional capabilities.

**Example:** A sidecar container in Kubernetes that provides monitoring or logging capabilities for the main application container.

**Real-Time Use Case:** Observability tools where a sidecar container collects metrics or logs from an application container.

---

Each design pattern serves different needs and scenarios, enhancing the flexibility, scalability, and maintainability of software systems. By choosing and implementing the appropriate patterns, developers can solve common problems in software design and architecture effectively.


Let's dive deeper into each of these backend communication design patterns, examining their concepts, practical implementations, and real-time use cases. I'll provide Java examples where applicable and describe how these patterns apply in different scenarios.

## 1. Request-Response

### Concept
The Request-Response pattern is the most fundamental client-server communication model where the client sends a request and waits for the server to respond. It is synchronous in nature, meaning the client waits for the server to finish processing before continuing.

### Example
Consider a REST API where a client requests user information:

- **Client**: Sends an HTTP GET request to `/api/users/123`.
- **Server**: Processes the request and responds with user data in JSON format.

```java
// Simple Java HTTP server example using HttpServer (Java SE)
import com.sun.net.httpserver.HttpServer;
import com.sun.net.httpserver.HttpHandler;
import com.sun.net.httpserver.HttpExchange;
import java.io.IOException;
import java.io.OutputStream;

public class SimpleHttpServer {
    public static void main(String[] args) throws IOException {
        HttpServer server = HttpServer.create(new InetSocketAddress(8080), 0);
        server.createContext("/api/users/123", new UserHandler());
        server.setExecutor(null);
        server.start();
    }

    static class UserHandler implements HttpHandler {
        public void handle(HttpExchange exchange) throws IOException {
            String response = "{\"id\":123, \"name\":\"John Doe\"}";
            exchange.sendResponseHeaders(200, response.getBytes().length);
            OutputStream os = exchange.getResponseBody();
            os.write(response.getBytes());
            os.close();
        }
    }
}
```

### Real-Time Use Case
In web browsing, a user’s browser makes HTTP requests to a web server, which responds with HTML content, images, or other resources necessary to render a web page.

---

## 2. Push

### Concept
Push is a communication pattern where the server sends data to the client without the client explicitly requesting it. This is useful for real-time updates where the server pushes new information as it becomes available.

### Example
Using WebSocket for real-time chat:

```java
// Java WebSocket server example using Tyrus
import javax.websocket.OnMessage;
import javax.websocket.server.ServerEndpoint;
import javax.websocket.Session;
import javax.websocket.OnOpen;
import javax.websocket.OnClose;
import javax.websocket.server.ServerContainer;
import javax.websocket.server.ServerEndpointConfig;
import java.io.IOException;
import java.util.concurrent.CopyOnWriteArraySet;

@ServerEndpoint("/chat")
public class ChatEndpoint {
    private static final CopyOnWriteArraySet<ChatEndpoint> chatEndpoints = new CopyOnWriteArraySet<>();

    @OnOpen
    public void onOpen(Session session) {
        chatEndpoints.add(this);
    }

    @OnMessage
    public void onMessage(String message) throws IOException {
        for (ChatEndpoint endpoint : chatEndpoints) {
            endpoint.sendMessage(message);
        }
    }

    @OnClose
    public void onClose(Session session) {
        chatEndpoints.remove(this);
    }

    private void sendMessage(String message) throws IOException {
        Session session = // obtain session
        session.getBasicRemote().sendText(message);
    }
}
```

### Real-Time Use Case
In real-time chat applications, the server pushes new messages to connected clients immediately when they are received.

---

## 3. Short Polling

### Concept
Short Polling involves the client repeatedly sending requests to the server at regular intervals to check for updates. This can result in a high volume of requests if the update frequency is high.

### Example
Polling for updates every 5 seconds:

```java
// Java HTTP client polling example using HttpURLConnection
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.net.HttpURLConnection;
import java.net.URL;

public class ShortPollingClient {
    public static void main(String[] args) throws Exception {
        while (true) {
            URL url = new URL("http://localhost:8080/api/updates");
            HttpURLConnection conn = (HttpURLConnection) url.openConnection();
            conn.setRequestMethod("GET");
            
            try (BufferedReader in = new BufferedReader(new InputStreamReader(conn.getInputStream()))) {
                String inputLine;
                while ((inputLine = in.readLine()) != null) {
                    System.out.println(inputLine);
                }
            }
            
            // Wait for 5 seconds before polling again
            Thread.sleep(5000);
        }
    }
}
```

### Real-Time Use Case
In live sports score updates, clients might poll the server every few seconds to check for the latest scores.

---

## 4. Long Polling

### Concept
Long Polling is a variation of polling where the server holds the request open until new data is available or a timeout occurs. This approach reduces the number of requests compared to short polling.

### Example
Java Servlet handling long polling:

```java
// Java Servlet for long polling
import javax.servlet.*;
import javax.servlet.http.*;
import java.io.IOException;
import java.util.concurrent.*;

public class LongPollingServlet extends HttpServlet {
    private static final int POLLING_TIMEOUT = 30000; // 30 seconds
    private static final BlockingQueue<String> messageQueue = new LinkedBlockingQueue<>();
    
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        response.setContentType("text/plain");
        response.setCharacterEncoding("UTF-8");
        
        try {
            String message = messageQueue.poll(POLLING_TIMEOUT, TimeUnit.MILLISECONDS);
            if (message == null) {
                response.getWriter().write("No new data");
            } else {
                response.getWriter().write(message);
            }
        } catch (InterruptedException e) {
            response.getWriter().write("Error");
        }
    }
    
    // Method to simulate pushing messages to the queue
    public static void pushMessage(String message) {
        messageQueue.offer(message);
    }
}
```

### Real-Time Use Case
Notification systems where the server holds the connection until a notification is available to send to the client.

---

## 5. Server-Sent Events (SSE)

### Concept
Server-Sent Events (SSE) allow the server to push updates to the client over a single, long-lived HTTP connection. Unlike WebSockets, SSE is unidirectional (server to client).

### Example
Java Servlet for SSE:

```java
// Java Servlet for SSE
import javax.servlet.*;
import javax.servlet.http.*;
import java.io.IOException;
import java.io.PrintWriter;

public class SseServlet extends HttpServlet {
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        response.setContentType("text/event-stream");
        response.setCharacterEncoding("UTF-8");
        
        PrintWriter writer = response.getWriter();
        
        // Simulate sending periodic updates
        new Thread(() -> {
            try {
                while (true) {
                    writer.write("data: " + "Update at " + System.currentTimeMillis() + "\n\n");
                    writer.flush();
                    Thread.sleep(5000); // Send updates every 5 seconds
                }
            } catch (InterruptedException e) {
                // Handle interruption
            }
        }).start();
    }
}
```

### Real-Time Use Case
Real-time dashboards where the server continuously sends updates to the client, such as live traffic reports.

---

## 6. Publish-Subscribe (Pub/Sub)

### Concept
The Publish-Subscribe pattern decouples producers (publishers) from consumers (subscribers) through a messaging broker or event bus. Publishers send messages to a topic, and subscribers receive messages from that topic.

### Example
Using Apache Kafka for Pub/Sub:

```java
// Kafka Producer
import org.apache.kafka.clients.producer.KafkaProducer;
import org.apache.kafka.clients.producer.ProducerRecord;
import java.util.Properties;

public class KafkaPublisher {
    public static void main(String[] args) {
        Properties props = new Properties();
        props.put("bootstrap.servers", "localhost:9092");
        props.put("key.serializer", "org.apache.kafka.common.serialization.StringSerializer");
        props.put("value.serializer", "org.apache.kafka.common.serialization.StringSerializer");

        KafkaProducer<String, String> producer = new KafkaProducer<>(props);
        producer.send(new ProducerRecord<>("my-topic", "key", "message"));
        producer.close();
    }
}

// Kafka Consumer
import org.apache.kafka.clients.consumer.ConsumerConfig;
import org.apache.kafka.clients.consumer.KafkaConsumer;
import org.apache.kafka.clients.consumer.ConsumerRecord;
import java.util.Collections;
import java.util.Properties;

public class KafkaSubscriber {
    public static void main(String[] args) {
        Properties props = new Properties();
        props.put("bootstrap.servers", "localhost:9092");
        props.put("group.id", "test-group");
        props.put("key.deserializer", "org.apache.kafka.common.serialization.StringDeserializer");
        props.put("value.deserializer", "org.apache.kafka.common.serialization.StringDeserializer");

        KafkaConsumer<String, String> consumer = new KafkaConsumer<>(props);
        consumer.subscribe(Collections.singletonList("my-topic"));

        while (true) {
            for (ConsumerRecord<String, String> record : consumer.poll(100).records("my-topic")) {
                System.out.printf("Received message: %s%n", record.value());
            }
        }
    }
}
```

### Real-Time Use Case
Event-driven systems like stock trading platforms where different components (traders, analytics) subscribe to different topics to react to market events.

---

## 7. Multiplexing and Demultiplexing

### Concept
Multiplexing combines multiple data streams into a single stream, while demultiplexing separates the combined stream back into individual data streams.

### Example
HTTP/2 multiplexing allows multiple requests and responses to be sent over a single TCP connection:

```java
// HTTP/2 Client (Java 11+ HTTP Client API)
import

 java.net.URI;
import java.net.http.HttpClient;
import java.net.http.HttpRequest;
import java.net.http.HttpResponse;

public class Http2Client {
    public static void main(String[] args) throws Exception {
        HttpClient client = HttpClient.newHttpClient();
        HttpRequest request1 = HttpRequest.newBuilder(URI.create("https://example.com/api/endpoint1")).build();
        HttpRequest request2 = HttpRequest.newBuilder(URI.create("https://example.com/api/endpoint2")).build();
        
        HttpResponse<String> response1 = client.send(request1, HttpResponse.BodyHandlers.ofString());
        HttpResponse<String> response2 = client.send(request2, HttpResponse.BodyHandlers.ofString());
        
        System.out.println("Response 1: " + response1.body());
        System.out.println("Response 2: " + response2.body());
    }
}
```

### Real-Time Use Case
Streaming video services where multiple video streams or data channels are managed over a single connection.

---

## 8. Stateful and Stateless

### Concept
- **Stateful**: The server maintains state across multiple requests. Useful for applications where user sessions or context are needed.
- **Stateless**: Each request is independent, and no session state is maintained on the server.

### Example
- **Stateful**: Java servlet maintaining user sessions:

```java
// Stateful servlet example
import javax.servlet.*;
import javax.servlet.http.*;
import java.io.IOException;

public class StatefulServlet extends HttpServlet {
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        HttpSession session = request.getSession();
        Integer count = (Integer) session.getAttribute("count");
        if (count == null) {
            count = 0;
        }
        count++;
        session.setAttribute("count", count);
        response.getWriter().write("Count: " + count);
    }
}
```

- **Stateless**: REST API where each request contains all necessary information:

```java
// Stateless REST API example
import javax.ws.rs.GET;
import javax.ws.rs.Path;
import javax.ws.rs.QueryParam;

@Path("/api")
public class StatelessApi {
    @GET
    @Path("/echo")
    public String echo(@QueryParam("message") String message) {
        return "Echo: " + message;
    }
}
```

### Real-Time Use Case
- **Stateful**: E-commerce websites that track user carts and sessions.
- **Stateless**: RESTful services where each request is independent and carries all needed context.

---

## 9. Sidecar Pattern

### Concept
The Sidecar pattern involves deploying an additional component (sidecar) alongside the main application container to provide supplementary features like monitoring, logging, or security.

### Example
Kubernetes sidecar container for logging:

```yaml
# Kubernetes Pod configuration with a sidecar container
apiVersion: v1
kind: Pod
metadata:
  name: my-app
spec:
  containers:
  - name: main-app
    image: my-app-image
    ports:
    - containerPort: 8080
  - name: logging-sidecar
    image: logging-agent-image
    volumeMounts:
    - name: log-volume
      mountPath: /var/log/my-app
  volumes:
  - name: log-volume
    emptyDir: {}
```

### Real-Time Use Case
Monitoring and logging where a sidecar container collects logs from the main application container and sends them to a centralized logging system.

---

These backend communication design patterns address various needs for data exchange and system interactions, each with its own strengths and ideal use cases. Understanding these patterns helps in designing scalable, efficient, and maintainable systems.
