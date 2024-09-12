
# React Interview Questions - Table of Contents

| #   | Question |
|-----|----------|
||**Core React**|
| 1   | [What is React?](#1-what-is-react) |
| 2   | [What are the major features of React?](#2-what-are-the-major-features-of-react) |
| 3   | [What is JSX?](#3-what-is-jsx) |
| 4   | [What is the difference between Element and Component?](#4-what-is-the-difference-between-element-and-component) |
| 5   | [How to create components in React?](#5-how-to-create-components-in-react) |
| 6   | [When to use a Class Component over a Function Component?](#6-when-to-use-a-class-component-over-a-function-component) |
| 7   | [What are Pure Components?](#7-what-are-pure-components) |
| 8   | [What is state in React?](#8-what-is-state-in-react) |
| 9   | [What are props in React?](#9-what-are-props-in-react) |
| 10  | [What is the difference between state and props?](#10-what-is-the-difference-between-state-and-props) |
| 11  | [Why should we not update the state directly?](#11-why-should-we-not-update-the-state-directly) |
| 12  | [What is the purpose of callback function as an argument of setState()?](#12-what-is-the-purpose-of-callback-function-as-an-argument-of-setstate) |
| 13  | [What is the difference between HTML and React event handling?](#13-what-is-the-difference-between-html-and-react-event-handling) |
| 14  | [How to bind methods or event handlers in JSX callbacks?](#14-how-to-bind-methods-or-event-handlers-in-jsx-callbacks) |
| 15  | [How to pass a parameter to an event handler or callback?](#15-how-to-pass-a-parameter-to-an-event-handler-or-callback) |
| 16  | [What are synthetic events in React?](#16-what-are-synthetic-events-in-react) |
| 17  | [What are inline conditional expressions?](#17-what-are-inline-conditional-expressions) |
| 18  | [What is "key" prop and what is the benefit of using it in arrays of elements?](#18-what-is-key-prop-and-what-is-the-benefit-of-using-it-in-arrays-of-elements) |
| 19  | [What is the use of refs?](#19-what-is-the-use-of-refs) |
| 20  | [How to create refs?](#20-how-to-create-refs) |
| 21  | [What are forward refs?](#21-what-are-forward-refs) |
| 22  | [Which is preferred option with callback refs and findDOMNode()?](#22-which-is-preferred-option-with-callback-refs-and-finddomnode) |
| 23  | [Why are String Refs legacy?](#23-why-are-string-refs-legacy) |
| 24  | [What is Virtual DOM?](#24-what-is-virtual-dom) |
| 25  | [How Virtual DOM works?](#25-how-virtual-dom-works) |
| 26  | [What is the difference between Shadow DOM and Virtual DOM?](#26-what-is-the-difference-between-shadow-dom-and-virtual-dom) |
| 27  | [What is React Fiber?](#27-what-is-react-fiber) |
| 28  | [What is the main goal of React Fiber?](#28-what-is-the-main-goal-of-react-fiber) |
| 29  | [What are controlled components?](#29-what-are-controlled-components) |
| 30  | [What are uncontrolled components?](#30-what-are-uncontrolled-components) |
| 31  | [What is the difference between createElement and cloneElement?](#31-what-is-the-difference-between-createelement-and-cloneelement) |
| 32  | [What is Lifting State Up in React?](#32-what-is-lifting-state-up-in-react) |
| 33  | [What are the different phases of component lifecycle?](#33-what-are-the-different-phases-of-component-lifecycle) |
| 34  | [What are the lifecycle methods of React?](#34-what-are-the-lifecycle-methods-of-react) |
| 35  | [What are Higher-Order components?](#35-what-are-higher-order-components) |
| 36  | [How to create props proxy for HOC component?](#36-how-to-create-props-proxy-for-hoc-component) |
| 37  | [What is context?](#37-what-is-context) |
| 38  | [What is children prop?](#38-what-is-children-prop) |
| 39  | [How to write comments in React?](#39-how-to-write-comments-in-react) |
| 40  | [What is the purpose of using super constructor with props argument?](#40-what-is-the-purpose-of-using-super-constructor-with-props-argument) |
| 41  | [What is reconciliation?](#41-what-is-reconciliation) |
| 42  | [How to set state with a dynamic key name?](#42-how-to-set-state-with-a-dynamic-key-name) |
| 43  | [What would be the common mistake of function being called every time the component renders?](#43-what-would-be-the-common-mistake-of-function-being-called-every-time-the-component-renders) |
| 44  | [Is lazy function supports named exports?](#44-is-lazy-function-supports-named-exports) |
| 45  | [Why React uses className over class attribute?](#45-why-react-uses-classname-over-class-attribute) |
| 46  | [What are fragments?](#46-what-are-fragments) |
| 47  | [Why fragments are better than container divs?](#47-why-fragments-are-better-than-container-divs) |
| 48  | [What are portals in React?](#48-what-are-portals-in-react) |
| 49  | [What are stateless components?](#49-what-are-stateless-components) |
| 50  | [What are stateful components?](#50-what-are-stateful-components) |
| 51  | [How to apply validation on props in React?](#51-how-to-apply-validation-on-props-in-react) |
| 52  | [What are the advantages of React?](#52-what-are-the-advantages-of-react) |
| 53  | [What are the limitations of React?](#53-what-are-the-limitations-of-react) |
| 54  | [What are error boundaries in React v16?](#54-what-are-error-boundaries-in-react-v16) |
| 55  | [How error boundaries handled in React v15?](#55-how-error-boundaries-handled-in-react-v15) |
| 56  | [What are the recommended ways for static type checking?](#56-what-are-the-recommended-ways-for-static-type-checking) |
| 57  | [What is the use of react-dom package?](#57-what-is-the-use-of-react-dom-package) |
| 58  | [What is the purpose of render method of react-dom?](#58-what-is-the-purpose-of-render-method-of-react-dom) |
| 59  | [What is ReactDOMServer?](#59-what-is-reactdomserver) |
| 60  | [How to use InnerHtml in React?](#60-how-to-use-innerhtml-in-react) |
| 61  | [How to use styles in React?](#61-how-to-use-styles-in-react) |
| 62  | [How events are different in React?](#62-how-events-are-different-in-react) |
| 63  | [What will happen if you use setState in constructor?](#63-what-will-happen-if-you-use-setstate-in-constructor) |
| 64  | [What is the impact of indexes as keys?](#64-what-is-the-impact-of-indexes-as-keys) |
| 65  | [Is it good to use setState() in componentWillMount() method?](#65-is-it-good-to-use-setstate-in-componentwillmount-method) |
| 66  | [What will happen if you use props in initial state?](#66-what-will-happen-if-you-use-props-in-initial-state) |
| 67  | [How do you conditionally render components?](#67-how-do-you-conditionally-render-components) |
| 68  | [Why we need to be careful when spreading props on DOM elements?](#68-why-we-need-to-be-careful-when-spreading-props-on-dom-elements) |
| 69  | [How you use decorators in React?](#69-how-you-use-decorators-in-react) |
| 70  | [How do you memoize a component?](#70-how-do-you-memoize-a-component) |
| 71  | [How you implement Server-Side Rendering or SSR?](#71-how-you-implement-server-side-rendering-or-ssr) |
| 72  | [How to enable production mode in React?](#72-how-to-enable-production-mode-in-react) |
| 73  | [What is CRA and its benefits?](#73-what-is-cra-and-its-benefits) |
| 74  | [What is the lifecycle methods order in mounting?](#74-what-is-the-lifecycle-methods-order-in-mounting) |
| 75  | [What are the lifecycle methods going to be deprecated in React v16?](#75-what-are-the-lifecycle-methods-going-to-be-deprecated-in-react-v16) |
| 76  | [What is the purpose of getDerivedStateFromProps() lifecycle method?](#76-what-is-the-purpose-of-getderivedstatefromprops-lifecycle-method) |
| 77  | [What is the purpose of getSnapshotBeforeUpdate() lifecycle method?](#77-what-is-the-purpose-of-getsnapshotbeforeupdate-lifecycle-method) |
| 78  | [Do Hooks replace render props and higher order components?](#78-do-hooks-replace-render-props-and-higher-order-components) |
| 79  | [What is the recommended way for naming components?](#79-what-is-the-recommended-way-for-naming-components) |
| 80  | [What is the recommended ordering of methods in component class?](#80-what-is-the-recommended-ordering-of-methods-in-component-class) |
| 81  | [What is a switching component?](#81-what-is-a-switching-component) |
| 82  | [Why we need to pass a function to setState()?](#82-why-we-need-to-pass-a-function-to-setstate) |
| 83  | [What is strict mode in React?](#83-what-is-strict-mode-in-react) |
| 84  | [What are React Mixins?](#84-what-are-react-mixins) |
| 85  | [Why is isMounted() an anti-pattern and what is the proper solution?](#85-why-is-ismounted-an-anti-pattern-and-what-is-the-proper-solution) |
| 86  | [What are the Pointer Events supported in React?](#86-what-are-the-pointer-events-supported-in-react) |
| 87  | [Why should component names start with capital letter?](#87-why-should-component-names-start-with-capital-letter) |
| 88  | [Are custom DOM attributes supported in React v16?](#88-are-custom-dom-attributes-supported-in-react-v16) |
| 89  | [What is the difference between constructor and getInitialState?](#89-what-is-the-difference-between-constructor-and-getinitialstate) |
| 90  | [Can you force a component to re-render without calling setState?](#90-can-you-force-a-component-to-re-render-without-calling-setstate) |
| 91  | [What is the difference between super() and super(props) in React using ES6 classes?](#91-what-is-the-difference-between-super-and-superprops-in-react-using-es6-classes) |
| 92  | [How to loop inside JSX?](#92-how-to-loop-inside-jsx) |
| 93  | [How do you access props in attribute quotes?](#93-how-do-you-access-props-in-attribute-quotes) |
| 94  | [What is React PropType array with shape?](#94-what-is-react-proptype-array-with-shape) |
| 95  | [How to conditionally apply class attributes?](#95-how-to-conditionally-apply-class-attributes) |
| 96  | [What is the difference between React and ReactDOM?](#96-what-is-the-difference-between-react-and-reactdom) |
| 97  | [Why ReactDOM is separated from React?](#97-why-reactdom-is-separated-from-react) |
| 98  | [How to use React label element?](#98-how-to-use-react-label-element) |
| 99  | [How to combine multiple inline style objects?](#99-how-to-combine-multiple-inline-style-objects) |
| 100 | [How to re-render the view when the browser is resized?](#100-how-to-re-render-the-view-when-the-browser-is-resized) |
| 101 | [What is the difference between setState and replaceState methods?](#101-what-is-the-difference-between-setstate-and-replacestate-methods) |
| 102 | [How to listen to state changes?](#102-how-to-listen-to-state-changes) |
| 103 | [What is the recommended approach of removing an array element in react state?](#103-what-is-the-recommended-approach-of-removing-an-array-element-in-react-state) |
| 104 | [Is it possible to use React without rendering HTML?](#104-is-it-possible-to-use-react-without-rendering-html) |
| 105 | [How to pretty print JSON with React?](#105-how-to-pretty-print-json-with-react) |
| 106 | [Why you can't update props in React?](#106-why-you-cant-update-props-in-react) |
| 107 | [How to focus an input element on page load?](#107-how-to-focus-an-input-element-on-page-load) |
| 108 | [What are the possible ways of updating objects in state?](#108-what-are-the-possible-ways-of-updating-objects-in-state) |
| 110 | [How can we find the version of React at runtime in the browser?](#110-how-can-we-find-the-version-of-react-at-runtime-in-the-browser) |
| 111 | [What are the approaches to include polyfills in your create-react-app?](#111-what-are-the-approaches-to-include-polyfills-in-your-create-react-app) |
| 112 | [How to use https instead of http in create-react-app?](#112-how-to-use-https-instead-of-http-in-create-react-app) |
| 113 | [How to avoid using relative path imports in create-react-app?](#113-how-to-avoid-using-relative-path-imports-in-create-react-app) |
| 114 | [How to add Google Analytics for react-router?](#114-how-to-add-google-analytics-for-react-router) |
| 115 | [How to update a component every second?](#115-how-to-update-a-component-every-second) |
| 116 | [How do you apply vendor prefixes to inline styles in React?](#116-how-do-you-apply-vendor-prefixes-to-inline-styles-in-react) |
| 117 | [How to import and export components using react and ES6?](#117-how-to-import-and-export-components-using-react-and-es6) |
| 118 | [What are the exceptions on React component naming?](#118-what-are-the-exceptions-on-react-component-naming) |
| 119 | [Why is a component constructor called only once?](#119-why-is-a-component-constructor-called-only-once) |
| 120 | [How to define constants in React?](#120-how-to-define-constants-in-react) |
| 121 | [How to programmatically trigger click event in React?](#121-how-to-programmatically-trigger-click-event-in-react) |
| 122 | [Is it possible to use async/await in plain React?](#122-is-it-possible-to-use-asyncawait-in-plain-react) |
| 123 | [What are the common folder structures for React?](#123-what-are-the-common-folder-structures-for-react) |
| 124 | [What are the popular packages for animation?](#124-what-are-the-popular-packages-for-animation) |
| 125 | [What is the benefit of styles modules?](#125-what-is-the-benefit-of-styles-modules) |
| 126 | [What are the popular React-specific linters?](#126-what-are-the-popular-react-specific-linters) |
| 127 | [How to make AJAX call and In which component lifecycle methods should I make an AJAX call?](#127-how-to-make-ajax-call-and-in-which-component-lifecycle-methods-should-i-make-an-ajax-call) |
| 128 | [What are render props?](#128-what-are-render-props)|
| | **React Router** |
| 129 | [What is React Router?](#129-what-is-react-router) |
| 130 | [How React Router is different from history library?](#130-how-react-router-is-different-from-history-library) |
| 131 | [What are the <Router> components of React Router v4?](#131-what-are-the-router-components-of-react-router-v4) |
| 132 | [What is the purpose of push and replace methods of history?](#132-what-is-the-purpose-of-push-and-replace-methods-of-history) |
| 133 | [How do you programmatically navigate using React Router v4?](#133-how-do-you-programmatically-navigate-using-react-router-v4) |
| 134 | [How to get query parameters in React Router v4?](#134-how-to-get-query-parameters-in-react-router-v4) |
| 135 | [Why you get "Router may have only one child element" warning?](#135-why-you-get-router-may-have-only-one-child-element-warning) |
| 136 | [How to pass params to history.push method in React Router v4?](#136-how-to-pass-params-to-historypush-method-in-react-router-v4) |
| 137 | [How to implement default or NotFound page?](#137-how-to-implement-default-or-notfound-page) |
| 138 | [How to get history on React Router v4?](#138-how-to-get-history-on-react-router-v4) |
| 139 | [How to perform automatic redirect after login?](#139-how-to-perform-automatic-redirect-after-login)|
| #   | **React Internationalization** |
| 140 | [What is React-Intl?](#140-what-is-react-intl) |
| 141 | [What are the main features of React Intl?](#141-what-are-the-main-features-of-react-intl) |
| 142 | [What are the two ways of formatting in React Intl?](#142-what-are-the-two-ways-of-formatting-in-react-intl) |
| 143 | [How to use FormattedMessage as placeholder using React Intl?](#143-how-to-use-formattedmessage-as-placeholder-using-react-intl) |
| 144 | [How to access current locale with React Intl?](#144-how-to-access-current-locale-with-react-intl) |
| 145 | [How to format date using React Intl?](#145-how-to-format-date-using-react-intl)|
| | **React Testing** |
| 146 | [What is Shallow Renderer in React testing?](#146-what-is-shallow-renderer-in-react-testing) |
| 147 | [What is TestRenderer package in React?](#147-what-is-testrenderer-package-in-react) |
| 148 | [What is the purpose of ReactTestUtils package?](#148-what-is-the-purpose-of-reacttestutils-package) |
| 149 | [What is Jest?](#149-what-is-jest) |
| 150 | [What are the advantages of Jest over Jasmine?](#150-what-are-the-advantages-of-jest-over-jasmine) |
| 151 | [Give a simple example of Jest test case](#151-give-a-simple-example-of-jest-test-case)|
| | **React Redux** |
| 152 | [What is Flux?](#152-what-is-flux) |
| 153 | [What is Redux?](#153-what-is-redux) |
| 154 | [What are the core principles of Redux?](#154-what-are-the-core-principles-of-redux) |
| 155 | [What are the downsides of Redux compared to Flux?](#155-what-are-the-downsides-of-redux-compared-to-flux) |
| 156 | [What is the difference between mapStateToProps() and mapDispatchToProps()?](#156-what-is-the-difference-between-mapstatetoprops-and-mapdispatchtoprops) |
| 157 | [Can I dispatch an action in reducer?](#157-can-i-dispatch-an-action-in-reducer) |
| 158 | [How to access Redux store outside a component?](#158-how-to-access-redux-store-outside-a-component) |
| 159 | [What are the drawbacks of MVW pattern?](#159-what-are-the-drawbacks-of-mvw-pattern) |
| 160 | [Are there any similarities between Redux and RxJS?](#160-are-there-any-similarities-between-redux-and-rxjs) |
| 161 | [How to dispatch an action on load?](#161-how-to-dispatch-an-action-on-load) |
| 162 | [How to use connect from React Redux?](#162-how-to-use-connect-from-react-redux) |
| 163 | [How to reset state in Redux?](#163-how-to-reset-state-in-redux) |
| 164 | [What's the purpose of @ symbol in the redux connect decorator?](#164-whats-the-purpose-of-at-symbol-in-the-redux-connect-decorator) |
| 165 | [What is the difference between React context and React Redux?](#165-what-is-the-difference-between-react-context-and-react-redux) |
| 166 | [Why are Redux state functions called reducers?](#166-why-are-redux-state-functions-called-reducers) |
| 167 | [How to make AJAX request in Redux?](#167-how-to-make-ajax-request-in-redux) |
| 168 | [Should I keep all component's state in Redux store?](#168-should-i-keep-all-components-state-in-redux-store) |
| 169 | [What is the proper way to access Redux store?](#169-what-is-the-proper-way-to-access-redux-store) |
| 170 | [What is the difference between component and container in React Redux?](#170-what-is-the-difference-between-component-and-container-in-react-redux) |
| 171 | [What is the purpose of constants in Redux?](#171-what-is-the-purpose-of-constants-in-redux) |
| 172 | [What are the different ways to write mapDispatchToProps()?](#172-what-are-the-different-ways-to-write-mapdispatchtoprops) |
| 173 | [What is the use of the ownProps parameter in mapStateToProps() and mapDispatchToProps()?](#173-what-is-the-use-of-the-ownprops-parameter-in-mapstatetoprops-and-mapdispatchtoprops) |
| 174 | [How to structure Redux top level directories?](#174-how-to-structure-redux-top-level-directories) |
| 175 | [What is redux-saga?](#175-what-is-redux-saga) |
| 176 | [What is the mental model of redux-saga?](#176-what-is-the-mental-model-of-redux-saga) |
| 177 | [What are the differences between call and put in redux-saga?](#177-what-are-the-differences-between-call-and-put-in-redux-saga) |
| 178 | [What is Redux Thunk?](#178-what-is-redux-thunk) |
| 179 | [What are the differences between redux-saga and redux-thunk?](#179-what-are-the-differences-between-redux-saga-and-redux-thunk) |
| 180 | [What is Redux DevTools?](#180-what-is-redux-devtools) |
| 181 | [What are the features of Redux DevTools?](#181-what-are-the-features-of-redux-devtools) |
| 182 | [What are Redux selectors and why use them?](#182-what-are-redux-selectors-and-why-use-them) |
| 183 | [What is Redux Form?](#183-what-is-redux-form) |
| 184 | [What are the main features of Redux Form?](#184-what-are-the-main-features-of-redux-form) |
| 185 | [How to add multiple middlewares to Redux?](#185-how-to-add-multiple-middlewares-to-redux) |
| 186 | [How to set initial state in Redux?](#186-how-to-set-initial-state-in-redux) |
| 187 | [How Relay is different from Redux?](#187-how-relay-is-different-from-redux) |
| 188 | [What is an action in Redux?](#188-what-is-an-action-in-redux)|
| | **React Native** |
| 188 | [What is the difference between React Native and React?](#188-what-is-the-difference-between-react-native-and-react) |
| 189 | [How to test React Native apps?](#189-how-to-test-react-native-apps) |
| 190 | [How to do logging in React Native?](#190-how-to-do-logging-in-react-native) |
| 191 | [How to debug your React Native?](#191-how-to-debug-your-react-native)|
| | **React Supported Libraries and Integration** |
| 192 | [What is reselect and how it works?](#192-what-is-reselect-and-how-it-works) |
| 193 | [What is Flow?](#193-what-is-flow) |
| 194 | [What is the difference between Flow and PropTypes?](#194-what-is-the-difference-between-flow-and-proptypes) |
| 195 | [How to use font-awesome icons in React?](#195-how-to-use-font-awesome-icons-in-react) |
| 196 | [What is React Dev Tools?](#196-what-is-react-dev-tools) |
| 197 | [Why is DevTools not loading in Chrome for local files?](#197-why-is-devtools-not-loading-in-chrome-for-local-files) |
| 198 | [How to use Polymer in React?](#198-how-to-use-polymer-in-react) |
| 199 | [What are the advantages of React over Vue.js?](#199-what-are-the-advantages-of-react-over-vuejs) |
| 200 | [What is the difference between React and Angular?](#200-what-is-the-difference-between-react-and-angular)|
| #   | **Miscellaneous** |
| 201 | [Why React tab is not showing up in DevTools?](#201-why-react-tab-is-not-showing-up-in-devtools) |
| 202 | [What are styled components?](#202-what-are-styled-components) |
| 203 | [Give an example of Styled Components?](#203-give-an-example-of-styled-components) |
| 204 | [What is Relay?](#204-what-is-relay) |
| 205 | [How to use TypeScript in create-react-app application?](#205-how-to-use-typescript-in-create-react-app-application) |
| 206 | [What are the main features of reselect library?](#206-what-are-the-main-features-of-reselect-library) |
| 207 | [Give an example of reselect usage?](#207-give-an-example-of-reselect-usage) |
| 209 | [Does the statics object work with ES6 classes in React?](#209-does-the-statics-object-work-with-es6-classes-in-react) |
| 210 | [Can Redux only be used with React?](#210-can-redux-only-be-used-with-react) |
| 211 | [Do you need to have a particular build tool to use Redux?](#211-do-you-need-to-have-a-particular-build-tool-to-use-redux) |
| 212 | [How Redux Form initialValues get updated from state?](#212-how-redux-form-initialvalues-get-updated-from-state) |
| 213 | [How React PropTypes allow different type for one prop?](#213-how-react-proptypes-allow-different-type-for-one-prop) |
| 214 | [Can I import an SVG file as react component?](#214-can-i-import-an-svg-file-as-react-component) |
| 215 | [Why are inline ref callbacks or functions not recommended?](#215-why-are-inline-ref-callbacks-or-functions-not-recommended) |
| 216 | [What is render hijacking in React?](#216-what-is-render-hijacking-in-react) |
| 217 | [What are HOC factory implementations?](#217-what-are-hoc-factory-implementations) |
| 218 | [How to pass numbers to React component?](#218-how-to-pass-numbers-to-react-component) |
| 219 | [Do I need to keep all my state into Redux? Should I ever use react internal state?](#219-do-i-need-to-keep-all-my-state-into-redux-should-i-ever-use-react-internal-state) |
| 220 | [What is the purpose of registerServiceWorker in React?](#220-what-is-the-purpose-of-registerserviceworker-in-react) |
| 221 | [What is React memo function?](#221-what-is-react-memo-function) |
| 222 | [What is React lazy function?](#222-what-is-react-lazy-function) |
| 223 | [How to prevent unnecessary updates using setState?](#223-how-to-prevent-unnecessary-updates-using-setstate) |
| 224 | [How do you render Array, Strings and Numbers in React 16 Version?](#224-how-do-you-render-array-strings-and-numbers-in-react-16-version) |
| 225 | [How to use class field declarations syntax in React classes?](#225-how-to-use-class-field-declarations-syntax-in-react-classes) |
| 226 | [What are hooks?](#226-what-are-hooks) |
| 227 | [What are the rules needs to follow for hooks?](#227-what-are-the-rules-needs-to-follow-for-hooks) |
| 228 | [How to ensure hooks followed the rules in your project?](#228-how-to-ensure-hooks-followed-the-rules-in-your-project) |
| 229 | [What are the differences between Flux and Redux?](#229-what-are-the-differences-between-flux-and-redux) |
| 230 | [What are the benefits of React Router V4?](#230-what-are-the-benefits-of-react-router-v4) |
| 231 | [Can you describe about componentDidCatch lifecycle method signature?](#231-can-you-describe-about-componentdidcatch-lifecycle-method-signature) |
| 232 | [In which scenarios error boundaries do not catch errors?](#232-in-which-scenarios-error-boundaries-do-not-catch-errors) |
| 233 | [Why do not you need error boundaries for event handlers?](#233-why-do-not-you-need-error-boundaries-for-event-handlers) |
| 234 | [What is the difference between try catch block and error boundaries?](#234-what-is-the-difference-between-try-catch-block-and-error-boundaries) |
| 235 | [What is the behavior of uncaught errors in react 16?](#235-what-is-the-behavior-of-uncaught-errors-in-react-16) |
| 236 | [What is the proper placement for error boundaries?](#236-what-is-the-proper-placement-for-error-boundaries) |
| 237 | [What is the benefit of component stack trace from error boundary?](#237-what-is-the-benefit-of-component-stack-trace-from-error-boundary) |
| 238 | [What is the required method to be defined for a class component?](#238-what-is-the-required-method-to-be-defined-for-a-class-component) |
| 239 | [What are the possible return types of render method?](#239-what-are-the-possible-return-types-of-render-method) |
| 240 | [What is the main purpose of constructor?](#240-what-is-the-main-purpose-of-constructor) |
| 241 | [Is it mandatory to define constructor for React component?](#241-is-it-mandatory-to-define-constructor-for-react-component) |
| 242 | [What are default props?](#242-what-are-default-props) |
| 243 | [Why should not call setState in componentWillUnmount?](#243-why-should-not-call-setstate-in-componentwillunmount) |
| 244 | [What is the purpose of getDerivedStateFromError?](#244-what-is-the-purpose-of-getderivedstatefromerror) |
| 245 | [What is the methods order when component re-rendered?](#245-what-is-the-methods-order-when-component-re-rendered) |
| 246 | [What are the methods invoked during error handling?](#246-what-are-the-methods-invoked-during-error-handling) |
| 247 | [What is the purpose of displayName class property?](#247-what-is-the-purpose-of-displayname-class-property) |
| 248 | [What is the browser support for react applications?](#248-what-is-the-browser-support-for-react-applications) |
| 249 | [What is the purpose of unmountComponentAtNode method?](#249-what-is-the-purpose-of-unmountcomponentatnode-method) |
| 250 | [What is code-splitting?](#250-what-is-code-splitting) |
| 251 | [What is the benefit of strict mode?](#251-what-is-the-benefit-of-strict-mode) |
| 252 | [What are Keyed Fragments?](#252-what-are-keyed-fragments) |
| 253 | [Does React support all HTML attributes?](#253-does-react-support-all-html-attributes) |
| 254 | [What are the limitations with HOCs?](#254-what-are-the-limitations-with-hocs) |
| 255 | [How to debug forwardRefs in DevTools?](#255-how-to-debug-forwardrefs-in-devtools) |
| 256 | [When component props defaults to true?](#256-when-component-props-defaults-to-true) |
| 257 | [What is NextJS and major features of it?](#257-what-is-nextjs-and-major-features-of-it) |
| 258 | [How do you pass an event handler to a component?](#258-how-do-you-pass-an-event-handler-to-a-component) |
| 259 | [Is it good to use arrow functions in render methods?](#259-is-it-good-to-use-arrow-functions-in-render-methods) |
| 260 | [How to prevent a function from being called multiple times?](#260-how-to-prevent-a-function-from-being-called-multiple-times) |
| 261 | [How JSX prevents Injection Attacks?](#261-how-jsx-prevents-injection-attacks) |
| 262 | [How do you update rendered elements?](#262-how-do-you-update-rendered-elements) |
| 263 | [How do you say that props are read only?](#263-how-do-you-say-that-props-are-read-only) |
| 264 | [How do you say that state updates are merged?](#264-how-do-you-say-that-state-updates-are-merged) |
| 265 | [How do you pass arguments to an event handler?](#265-how-do-you-pass-arguments-to-an-event-handler) |
| 266 | [How to prevent component from rendering?](#266-how-to-prevent-component-from-rendering) |
| 267 | [What are the conditions to safely use the index as a key?](#267-what-are-the-conditions-to-safely-use-the-index-as-a-key) |
| 268 | [Is it keys should be globally unique?](#268-is-it-keys-should-be-globally-unique) |
| 269 | [What is the popular choice for form handling?](#269-what-is-the-popular-choice-for-form-handling) |
| 270 | [What are the advantages of formik over redux form library?](#270-what-are-the-advantages-of-formik-over-redux-form-library) |
| 271 | [Why do you not required to use inheritance?](#271-why-do-you-not-required-to-use-inheritance) |
| 272 | [Can I use web components in react application?](#272-can-i-use-web-components-in-react-application) |
| 273 | [What is dynamic import?](#273-what-is-dynamic-import) |
| 274 | [What are loadable components?](#274-what-are-loadable-components) |
| 275 | [What is suspense component?](#275-what-is-suspense-component) |
| 276 | [What is route based code splitting?](#276-what-is-route-based-code-splitting) |
| 277 | [Give an example on How to use context?](#277-give-an-example-on-how-to-use-context) |
| 278 | [What is the purpose of default value in context?](#278-what-is-the-purpose-of-default-value-in-context) |
| 279 | [How do you use contextType?](#279-how-do-you-use-contexttype) |
| 280 | [What is a consumer?](#280-what-is-a-consumer) |
| 281 | [How do you solve performance corner cases while using context?](#281-how-do-you-solve-performance-corner-cases-while-using-context) |
| 282 | [What is the purpose of forward ref in HOCs?](#282-what-is-the-purpose-of-forward-ref-in-hocs) |
| 283 | [Is it ref argument available for all functions or class components?](#283-is-it-ref-argument-available-for-all-functions-or-class-components) |
| 284 | [Why do you need additional care for component libraries while using forward refs?](#284-why-do-you-need-additional-care-for-component-libraries-while-using-forward-refs) |
| 285 | [How to create react class components without ES6?](#285-how-to-create-react-class-components-without-es6) |
| 286 | [Is it possible to use react without JSX?](#286-is-it-possible-to-use-react-without-jsx) |
| 287 | [What is diffing algorithm?](#287-what-is-diffing-algorithm) |
| 288 | [What are the rules covered by diffing algorithm?](#288-what-are-the-rules-covered-by-diffing-algorithm) |
| 289 | [When do you need to use refs?](#289-when-do-you-need-to-use-refs) |
| 290 | [Is it prop must be named as render for render props?](#290-is-it-prop-must-be-named-as-render-for-render-props) |
| 291 | [What are the problems of using render props with pure components?](#291-what-are-the-problems-of-using-render-props-with-pure-components) |
| 292 | [How do you create HOC using render props?](#292-how-do-you-create-hoc-using-render-props) |
| 293 | [What is windowing technique?](#293-what-is-windowing-technique) |
| 294 | [How do you print falsy values in JSX?](#294-how-do-you-print-falsy-values-in-jsx) |
| 295 | [What is the typical use case of portals?](#295-what-is-the-typical-use-case-of-portals) |
| 296 | [How do you set default value for uncontrolled component?](#296-how-do-you-set-default-value-for-uncontrolled-component) |
| 297 | [What is your favorite React stack?](#297-what-is-your-favorite-react-stack) |
| 298 | [What is the difference between Real DOM and Virtual DOM?](#298-what-is-the-difference-between-real-dom-and-virtual-dom) |
| 299 | [How to add Bootstrap to a react application?](#299-how-to-add-bootstrap-to-a-react-application) |
| 300 | [Can you list the default events provided by React?](#300-can-you-list-the-default-events-provided-by-react) |
| 301 | [Is it recommended to use CSS In JS technique in React?](#301-is-it-recommended-to-use-css-in-js-technique-in-react) |
| 302 | [Do I need to rewrite all my class components with hooks?](#302-do-i-need-to-rewrite-all-my-class-components-with-hooks) |
| 303 | [How to fetch data with React Hooks?](#303-how-to-fetch-data-with-react-hooks) |
| 304 | [Do Hooks cover all use cases for classes?](#304-do-hooks-cover-all-use-cases-for-classes) |
| 305 | [What is the stable release for hooks support?](#305-what-is-the-stable-release-for-hooks-support) |
| 306 | [Why do we use array destructuring (square brackets notation) in useState?](#306-why-do-we-use-array-destructuring-square-brackets-notation-in-usestate) |
| 307 | [What are the sources used for introducing hooks?](#307-what-are-the-sources-used-for-introducing-hooks) |
| 308 | [How do you access imperative API of web components?](#308-how-do-you-access-imperative-api-of-web-components) |
| 309 | [What is Formik?](#309-what-is-formik) |
| 310 | [What are typical middleware choices for handling asynchronous calls in Redux?](#310-what-are-typical-middleware-choices-for-handling-asynchronous-calls-in-redux) |
| 311 | [Do browsers understand JSX code?](#311-do-browsers-understand-jsx-code) |
| 312 | [Describe the data flow in React?](#312-describe-the-data-flow-in-react) |
| 313 | [What is React Scripts?](#313-what-is-react-scripts) |
| 314 | [What are the features of Create React App?](#314-what-are-the-features-of-create-react-app) |
| 315 | [What is the purpose of renderToNodeStream method?](#315-what-is-the-purpose-of-rendertonodestream-method) |
| 316 | [What is MobX?](#316-what-is-mobx) |
| 317 | [What are the differences between Redux and MobX?](#317-what-are-the-differences-between-redux-and-mobx) |
| 318 | [Should I learn ES6 before learning ReactJS?](#318-should-i-learn-es6-before-learning-reactjs) |
| 319 | [What is Concurrent Rendering?](#319-what-is-concurrent-rendering) |
| 320 | [What is the difference between async mode and concurrent mode?](#320-what-is-the-difference-between-async-mode-and-concurrent-mode) |
| 321 | [Can I use JavaScript URLs in React 16.9?](#321-can-i-use-javascript-urls-in-react-169) |
| 322 | [What is the purpose of eslint plugin for hooks?](#322-what-is-the-purpose-of-eslint-plugin-for-hooks) |
| 323 | [What is the difference between Imperative and Declarative in React?](#323-what-is-the-difference-between-imperative-and-declarative-in-react) |
| 324 | [What are the benefits of using TypeScript with ReactJS?](#324-what-are-the-benefits-of-using-typescript-with-reactjs) |
| 325 | [How do you make sure that user remains authenticated on page refresh while using Context API State Management?](#325-how-do-you-make-sure-that-user-remains-authenticated-on-page-refresh-while-using-context-api-state-management) |
| 326 | [What are the benefits of the new JSX transform?](#326-what-are-the-benefits-of-the-new-jsx-transform) |
| 327 | [How does the new JSX transform differ from the old transform?](#327-how-does-the-new-jsx-transform-differ-from-the-old-transform) |


### 1. What is React?
**Definition:** React is a JavaScript library for building user interfaces, particularly for single-page applications where a dynamic and interactive user experience is required.

### 2. What are the major features of React?
- **Component-Based Architecture:** UI is divided into reusable components.
- **JSX:** A syntax extension that allows writing HTML-like code in JavaScript.
- **Virtual DOM:** Efficient updates to the real DOM by using a virtual representation.
- **One-Way Data Binding:** Data flows in one direction, making it easier to understand how data changes affect the UI.
- **Hooks:** Functions that let you use state and other React features in functional components.

### 3. What is JSX?
**Definition:** JSX (JavaScript XML) is a syntax extension for JavaScript that allows you to write HTML-like code within JavaScript. It is then compiled to JavaScript functions.

**Example:**
```jsx
const element = <h1>Hello, world!</h1>;
```

### 4. What is the difference between Element and Component?
- **Element:** A plain object describing what should appear in the UI. For example, `<div>Hello</div>` is an element.
- **Component:** A function or class that optionally accepts inputs (props) and returns a React element describing what should appear on the screen. Components can be reused and are more complex than elements.

### 5. How to create components in React?
- **Functional Component:**
```jsx
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```
- **Class Component:**
```jsx
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}
```

### 6. When to use a Class Component over a Function Component?
- **Class Component:** Use when you need to use lifecycle methods or manage state using `this.state` and `this.setState()`.
- **Function Component:** Preferable for simpler components, especially when using React Hooks for managing state and side effects.

### 7. What are Pure Components?
**Definition:** Pure components are components that implement `shouldComponentUpdate` with a shallow prop and state comparison to prevent unnecessary re-renders.

**Example:**
```jsx
class MyComponent extends React.PureComponent {
  render() {
    // Component logic here
  }
}
```

### 8. What is state in React?
**Definition:** State is a built-in object that stores property values that belong to a component. State can be modified using `setState()` in class components or `useState()` in functional components.

### 9. What are props in React?
**Definition:** Props (short for properties) are read-only attributes passed from a parent component to a child component to configure or render it. Props cannot be changed by the child component.

### 10. What is the difference between state and props?
- **State:** Managed within a component and can change over time. Used for dynamic data.
- **Props:** Passed from parent to child components and are immutable within the child component. Used for static or external data.

### 11. Why should we not update the state directly?
**Reason:** Directly modifying state bypasses React’s state management and lifecycle methods, which can lead to unpredictable behavior and rendering issues. Always use `setState()` or `useState()` for updates.

### 12. What is the purpose of the callback function as an argument of `setState()`?
**Purpose:** To perform actions based on the state update. It runs after the state has been updated and the component has re-rendered.

**Example:**
```jsx
this.setState({ count: this.state.count + 1 }, () => {
  console.log('State updated:', this.state.count);
});
```

### 13. What is the difference between HTML and React event handling?
**Difference:** 
- **HTML:** Uses string-based event handling attributes (e.g., `onclick="handleClick()"`).
- **React:** Uses a camelCase syntax and functions (e.g., `onClick={this.handleClick}`).

### 14. How to bind methods or event handlers in JSX callbacks?
**Options:**
- **Bind in constructor:**
```jsx
constructor(props) {
  super(props);
  this.handleClick = this.handleClick.bind(this);
}
```
- **Arrow functions in render:**
```jsx
<button onClick={() => this.handleClick()}>Click</button>
```

### 15. How to pass a parameter to an event handler or callback?
**Example:**
```jsx
<button onClick={() => this.handleClick(param)}>Click</button>
```

### 16. What are synthetic events in React?
**Definition:** Synthetic events are React’s cross-browser wrapper around the browser’s native events. They are normalized and consistent across different browsers.

### 17. What are inline conditional expressions?
**Definition:** Techniques for conditionally rendering elements in JSX using ternary operators or logical AND (`&&`).

**Example:**
```jsx
{isLoggedIn ? <LogoutButton /> : <LoginButton />}
```

### 18. What is "key" prop and what is the benefit of using it in arrays of elements?
**Definition:** The `key` prop helps React identify which items have changed, are added, or are removed. It improves performance by optimizing the re-rendering of lists.

### 19. What is the use of refs?
**Definition:** Refs are used to access and interact directly with DOM elements or React component instances.

### 20. How to create refs?
**Example:**
```jsx
const inputRef = useRef(null);
<input ref={inputRef} />
```

### 21. What are forward refs?
**Definition:** Forward refs allow components to forward refs to their children, enabling access to child DOM nodes or components.

**Example:**
```jsx
const FancyInput = forwardRef((props, ref) => (
  <input ref={ref} {...props} />
));
```

### 22. Which is the preferred option with callback refs and `findDOMNode()`?
**Preferred:** Callback refs are preferred as `findDOMNode()` is considered legacy and less efficient.

### 23. Why are String Refs legacy?
**Reason:** String refs are considered legacy because they are less flexible and less reliable compared to callback refs and `React.createRef()`.

### 24. What is Virtual DOM?
**Definition:** The Virtual DOM is a lightweight copy of the real DOM. React uses it to optimize rendering by updating only the parts of the real DOM that have changed.

### 25. How Virtual DOM works?
**Process:**
1. **Render:** React creates a virtual representation of the UI.
2. **Diffing:** React compares the new virtual DOM with the previous one.
3. **Reconciliation:** React updates the real DOM based on the differences.

### 26. What is the difference between Shadow DOM and Virtual DOM?
- **Shadow DOM:** Encapsulates styles and structure of a component, providing a separate DOM tree.
- **Virtual DOM:** A performance optimization for updating the real DOM efficiently by minimizing direct manipulations.

### 27. What is React Fiber?
**Definition:** React Fiber is a complete rewrite of the React core algorithm that improves rendering performance and introduces features like incremental rendering and better support for async rendering.

### 28. What is the main goal of React Fiber?
**Goal:** To enable incremental rendering, allowing React to pause, abort, and continue rendering work, improving user experience and performance.

### 29. What are controlled components?
**Definition:** Controlled components are form elements whose value is controlled by React state. Changes are handled through event handlers.

**Example:**
```jsx
<input type="text" value={this.state.value} onChange={this.handleChange} />
```

### 30. What are uncontrolled components?
**Definition:** Uncontrolled components store their own state internally and access values through refs rather than state.

**Example:**
```jsx
<input type="text" ref={this.inputRef} />
```

### 31. What is the difference between `createElement` and `cloneElement`?
- **`createElement`:** Creates a new React element.
- **`cloneElement`:** Clones and returns a new element with additional props.

### 32. What is Lifting State Up in React?
**Definition:** Moving state from a child component to its parent so that multiple child components can share and synchronize the state.

### 33. What are the different phases of component lifecycle?
- **Mounting:** Component is being created and inserted into the DOM.
- **Updating:** Component is being re-rendered due to state or prop changes.
- **Unmounting:** Component is being removed from the DOM.

### 34. What are the lifecycle methods of React?
**Class Component Lifecycle Methods:**
- **Mounting:** `constructor()`, `componentDidMount()`
- **Updating:** `shouldComponentUpdate()`, `componentDidUpdate()`
- **Unmounting:** `componentWillUnmount()`

### 35. What are Higher-Order components?
**Definition:** Higher-Order Components (HOCs) are functions that take a component and return a new component with enhanced functionality.

**Example:**
```jsx
function withLogging(WrappedComponent) {
  return class extends React.Component {
    componentDidMount() {
      console.log('Component mounted');
    }
    render() {
      return <WrappedComponent {...this.props} />;
    }
  };
}
```

### 36. How to create props proxy for HOC component?
**Example:**
```jsx
const withPropsProxy = (WrappedComponent) => {
  return class extends React.Component {
    render() {
      const

 newProps = { ...this.props, newProp: 'value' };
      return <WrappedComponent {...newProps} />;
    }
  };
};
```

### 37. What is context?
**Definition:** Context provides a way to pass data through the component tree without having to pass props down manually at every level.

### 38. What is children prop?
**Definition:** The `children` prop is a special prop that allows components to pass nested elements to their children.

**Example:**
```jsx
function Container({ children }) {
  return <div>{children}</div>;
}
```

### 39. How to write comments in React?
**Syntax:**
```jsx
{/* This is a comment */}
```

### 40. What is the purpose of using super constructor with props argument?
**Purpose:** To initialize the parent class (React.Component) with the props, allowing access to `this.props` in the constructor of a class component.

**Example:**
```jsx
constructor(props) {
  super(props);
  this.state = { /* state initialization */ };
}
```

### 41. What is reconciliation?
**Definition:** Reconciliation is the process by which React updates the DOM with changes based on the virtual DOM’s diffing algorithm.

### 42. How to set state with a dynamic key name?
**Example:**
```jsx
this.setState(prevState => ({
  [dynamicKey]: newValue
}));
```

### 43. What would be the common mistake of a function being called every time the component renders?
**Mistake:** Defining a function inside the render method. This creates a new function on every render, causing unnecessary re-renders of child components.

### 44. Does `lazy` function support named exports?
**No:** `React.lazy` supports default exports only. Named exports should be wrapped in a default export.

### 45. Why does React use `className` over `class` attribute?
**Reason:** `class` is a reserved keyword in JavaScript, so React uses `className` to avoid conflicts.

### 46. What are fragments?
**Definition:** Fragments let you group multiple elements without adding extra nodes to the DOM.

**Example:**
```jsx
<>
  <Child1 />
  <Child2 />
</>
```

### 47. Why are fragments better than container divs?
**Reason:** Fragments do not add extra nodes to the DOM, which helps keep the DOM structure cleaner and avoids unnecessary elements.

### 48. What are portals in React?
**Definition:** Portals allow rendering children into a different part of the DOM outside of the parent component’s DOM hierarchy.

**Example:**
```jsx
ReactDOM.createPortal(child, container)
```

### 49. What are stateless components?
**Definition:** Stateless components are components that do not manage state and only rely on props for rendering.

**Example:**
```jsx
function StatelessComponent(props) {
  return <div>{props.text}</div>;
}
```

### 50. What are stateful components?
**Definition:** Stateful components manage their own state and use it to control rendering and behavior.

**Example:**
```jsx
class StatefulComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  render() {
    return <div>{this.state.count}</div>;
  }
}
```

### 51. How to apply validation on props in React?
**Method:** Use `PropTypes` to define expected types and required props.

**Example:**
```jsx
import PropTypes from 'prop-types';

MyComponent.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number
};
```

### 52. What are the advantages of React?
- **Component-Based Architecture:** Modular and reusable components.
- **Virtual DOM:** Efficient rendering and updates.
- **Declarative Syntax:** Easier to understand and debug.
- **Strong Community and Ecosystem:** Wide range of libraries and tools.

### 53. What are the limitations of React?
- **Learning Curve:** Requires understanding JSX, components, and state management.
- **Boilerplate:** Often involves additional setup and tooling.
- **SEO Challenges:** Client-side rendering can be challenging for SEO unless server-side rendering is used.

### 54. What are error boundaries in React v16?
**Definition:** Error boundaries are components that catch JavaScript errors anywhere in their child component tree and log those errors or display fallback UI.

**Example:**
```jsx
class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false };
  }

  static getDerivedStateFromError() {
    return { hasError: true };
  }

  componentDidCatch(error, info) {
    console.error(error, info);
  }

  render() {
    if (this.state.hasError) {
      return <h1>Something went wrong.</h1>;
    }

    return this.props.children;
  }
}
```

### 55. How were error boundaries handled in React v15?
**Answer:** React v15 did not have error boundaries. Error handling in v15 was typically done with try-catch blocks and error handling in lifecycle methods.

### 56. What are the recommended ways for static type checking?
- **PropTypes:** For runtime type checking of props.
- **TypeScript:** For static type checking and integrating types into your development workflow.

### 57. What is the use of `react-dom` package?
**Definition:** The `react-dom` package provides DOM-specific methods to mount and unmount React components and manage updates to the DOM.

### 58. What is the purpose of the `render` method of `react-dom`?
**Purpose:** To render a React component tree into the DOM.

**Example:**
```jsx
ReactDOM.render(<App />, document.getElementById('root'));
```

### 59. What is `ReactDOMServer`?
**Definition:** `ReactDOMServer` is used for server-side rendering of React components, allowing you to generate HTML on the server.

### 60. How to use `innerHTML` in React?
**Example:**
```jsx
<div dangerouslySetInnerHTML={{ __html: '<p>HTML content</p>' }} />
```
**Caution:** Use `dangerouslySetInnerHTML` sparingly to avoid XSS attacks.

### 61. How to use styles in React?
**Options:**
- **Inline Styles:**
```jsx
const style = { color: 'blue' };
<div style={style}>Hello</div>
```
- **CSS Modules:** 
```jsx
import styles from './styles.module.css';
<div className={styles.myClass}>Hello</div>
```
- **Styled Components:** Use libraries like `styled-components` for CSS-in-JS.

### 62. How are events different in React?
**Difference:** React wraps native events in synthetic events, which are normalized and consistent across browsers.

### 63. What will happen if you use `setState` in the constructor?
**Outcome:** Using `setState` in the constructor will not have any effect because the component is not yet mounted. Initialization of state should be done directly in the constructor.

### 64. What is the impact of indexes as keys?
**Impact:** Using array indexes as keys can lead to performance issues and component state problems, especially when items are reordered or removed. It’s better to use unique IDs.

### 65. Is it good to use `setState()` in `componentWillMount()` method?
**Answer:** No, `componentWillMount()` is deprecated. Use `componentDidMount()` for making changes to state or side effects.

### 66. What will happen if you use props in initial state?
**Answer:** It can lead to problems if the props change after initial render. Use `getDerivedStateFromProps` or `componentDidUpdate` for synchronizing state with props.

### 67. How do you conditionally render components?
**Methods:**
- **Ternary Operator:** 
```jsx
{isLoggedIn ? <LogoutButton /> : <LoginButton />}
```
- **Logical AND (`&&`):**
```jsx
{showContent && <Content />}
```

### 68. Why we need to be careful when spreading props on DOM elements?
**Reason:** Spreading props on DOM elements can inadvertently pass unwanted attributes or props to the DOM, leading to potential bugs or warnings.

### 69. How do you use decorators in React?
**Answer:** Decorators are a proposed feature and are not part of the core React library. They can be used with tools like Babel to modify class behavior.

### 70. How do you memoize a component?
**Methods:**
- **`React.memo`:** For functional components.
```jsx
const MemoizedComponent = React.memo(Component);
```
- **`useMemo` and `useCallback`:** For optimizing specific functions or values.

### 71. How do you implement Server-Side Rendering (SSR)?
**Method:** Use `ReactDOMServer.renderToString()` or frameworks like Next.js for server-side rendering to generate HTML on the server.

### 72. How to enable production mode in React?
**Method:** Set the `NODE_ENV` environment variable to `"production"` during build and deployment.

### 73. What is CRA and its benefits?
**Definition:** CRA (Create React App) is a tool for setting up a new React project with a modern build setup. Benefits include zero configuration, built-in development tools, and optimized builds.

### 74. What is the lifecycle methods order in mounting?
**Order:**
1. `constructor()`
2. `static getDerivedStateFromProps()`
3. `render()`
4. `componentDidMount()`

### 75. What lifecycle methods are

 going to be deprecated in React v16?
**Deprecated Methods:**
- `componentWillMount()`
- `componentWillReceiveProps()`
- `componentWillUpdate()`

### 76. What is the purpose of `getDerivedStateFromProps()` lifecycle method?
**Purpose:** To derive state from props before rendering. It’s called right before rendering, both on the initial mount and on subsequent updates.

### 77. What is the purpose of `getSnapshotBeforeUpdate()` lifecycle method?
**Purpose:** To capture some information from the DOM before it is potentially changed. Useful for reading layout information.

### 78. Do Hooks replace render props and higher-order components?
**Answer:** Hooks provide a simpler and more direct way to reuse stateful logic and side effects, which can often replace the need for render props and higher-order components.

### 79. What is the recommended way for naming components?
**Recommendation:** Use PascalCase for component names (e.g., `MyComponent`) to distinguish them from HTML elements and JavaScript functions.

### 80. What is the recommended ordering of methods in a component class?
**Recommended Order:**
1. Constructor
2. Static methods (e.g., `getDerivedStateFromProps`)
3. Lifecycle methods
4. Event handlers
5. Render method

### 81. What is a switching component?
**Definition:** A switching component (often used with React Router) renders different components based on the current URL or route.

### 82. Why do we need to pass a function to `setState()`?
**Reason:** To ensure that state updates are based on the previous state, especially when updates are asynchronous or depend on the current state.

### 83. What is Strict Mode in React?
**Definition:** Strict Mode is a development-only feature that helps identify potential problems in an application by activating additional checks and warnings.

### 84. What are React Mixins?
**Definition:** Mixins were a way to reuse code across multiple components but are now deprecated in favor of higher-order components and hooks.

### 85. Why is `isMounted()` an anti-pattern and what is the proper solution?
**Reason:** `isMounted()` is considered unreliable. Use `componentDidMount()` and `componentWillUnmount()` to handle setup and cleanup.

### 86. What are the Pointer Events supported in React?
**Supported Events:**
- `onPointerDown`
- `onPointerUp`
- `onPointerMove`
- `onPointerEnter`
- `onPointerLeave`
- `onPointerCancel`

### 87. Why should component names start with a capital letter?
**Reason:** Component names must start with a capital letter to distinguish them from HTML tags and to enable JSX to properly recognize them.

### 88. Are custom DOM attributes supported in React v16?
**Yes:** React v16 supports custom attributes as long as they do not clash with standard HTML attributes or React-specific attributes.

### 89. What is the difference between constructor and `getInitialState`?
- **Constructor:** Initializes state and binds methods in ES6 classes.
- **`getInitialState`:** Was used in React's earlier versions (before ES6 classes) to initialize state.

### 90. Can you force a component to re-render without calling `setState`?
**Method:** Yes, you can force a re-render by calling `forceUpdate()`, but this is generally discouraged. `setState` should be used for state changes.

### 91. What is the difference between `super()` and `super(props)` in React using ES6 classes?
- **`super()`:** Calls the parent class constructor without passing props.
- **`super(props)`:** Calls the parent class constructor and passes props, allowing access to `this.props` in the constructor.

### 92. How to loop inside JSX?
**Method:** Use JavaScript array methods like `map()` to iterate and render elements.

**Example:**
```jsx
const items = ['Item1', 'Item2', 'Item3'];
const listItems = items.map((item, index) => <li key={index}>{item}</li>);
return <ul>{listItems}</ul>;
```

### 93. How do you access props in attribute quotes?
**Example:**
```jsx
const Greeting = ({ name }) => <div>Hello, {name}</div>;
```

### 94. What is React PropType array with shape?
**Definition:** A way to validate the shape of array elements using PropTypes.

**Example:**
```jsx
MyComponent.propTypes = {
  items: PropTypes.arrayOf(PropTypes.shape({
    id: PropTypes.number,
    name: PropTypes.string
  }))
};
```

### 95. How to conditionally apply class attributes?
**Example:**
```jsx
const className = isActive ? 'active' : 'inactive';
<div className={className}>Content</div>
```

### 96. What is the difference between React and ReactDOM?
- **React:** Core library for building components and managing the virtual DOM.
- **ReactDOM:** Provides methods to render React components to the actual DOM.

### 97. Why is ReactDOM separated from React?
**Reason:** Separation allows React to focus on building components and managing state while ReactDOM handles the specific tasks related to DOM manipulation.

### 98. How to use React label element?
**Example:**
```jsx
<label htmlFor="inputId">Label</label>
<input id="inputId" />
```

### 99. How to combine multiple inline style objects?
**Example:**
```jsx
const style1 = { color: 'red' };
const style2 = { fontSize: '20px' };
const combinedStyle = { ...style1, ...style2 };

<div style={combinedStyle}>Styled Text</div>
```

### 100. How to re-render the view when the browser is resized?
**Method:** Use the `resize` event listener to handle window size changes.

**Example:**
```jsx
useEffect(() => {
  const handleResize = () => {
    // handle resize
  };

  window.addEventListener('resize', handleResize);

  return () => {
    window.removeEventListener('resize', handleResize);
  };
}, []);
```

### 101. What is the difference between `setState` and `replaceState` methods?
- **`setState`:** Merges the provided state into the current state.
  ```jsx
  this.setState({ name: 'John' });
  ```
- **`replaceState`:** Replaces the entire state with the provided state. Note that `replaceState` is deprecated in React and should not be used.
  ```jsx
  this.replaceState({ name: 'John' });
  ```

### 102. How to listen to state changes?
- **Method:** Use `componentDidUpdate` lifecycle method in class components or `useEffect` hook in function components to respond to state changes.
  ```jsx
  // Class Component
  componentDidUpdate(prevProps, prevState) {
    if (this.state.someValue !== prevState.someValue) {
      // handle state change
    }
  }

  // Function Component
  useEffect(() => {
    // handle state change
  }, [stateValue]);
  ```

### 103. What is the recommended approach of removing an array element in React state?
- **Method:** Use array methods like `filter()` to create a new array excluding the item you want to remove, and then update state with this new array.
  ```jsx
  this.setState(prevState => ({
    items: prevState.items.filter(item => item.id !== idToRemove)
  }));
  ```

### 104. Is it possible to use React without rendering HTML?
- **Answer:** Yes, React can be used for server-side rendering, generating components that don't directly render HTML but instead output JSON or other formats.

### 105. How to pretty print JSON with React?
- **Example:**
  ```jsx
  import React from 'react';

  function PrettyPrintJson({ data }) {
    return (
      <pre>{JSON.stringify(data, null, 2)}</pre>
    );
  }
  ```

### 106. Why you can't update props in React?
- **Reason:** Props are immutable and meant to be read-only. Components should use props to render data and can only change their internal state using `setState`.

### 107. How to focus an input element on page load?
- **Example:**
  ```jsx
  import React, { useRef, useEffect } from 'react';

  function MyComponent() {
    const inputRef = useRef(null);

    useEffect(() => {
      inputRef.current.focus();
    }, []);

    return <input ref={inputRef} />;
  }
  ```

### 108. What are the possible ways of updating objects in state?
- **Methods:**
  - **Using `setState` in Class Components:**
    ```jsx
    this.setState(prevState => ({
      user: { ...prevState.user, name: 'John' }
    }));
    ```
  - **Using `useState` in Function Components:**
    ```jsx
    setUser(prevUser => ({ ...prevUser, name: 'John' }));
    ```

### 110. How can we find the version of React at runtime in the browser?
- **Method:**
  ```jsx
  console.log(React.version);
  ```

### 111. What are the approaches to include polyfills in your Create React App?
- **Methods:**
  - **Configure `browserslist`:** In `package.json`, set up the `browserslist` key to specify supported browsers. CRA automatically includes necessary polyfills.
  - **Manual Inclusion:** Use libraries like `core-js` and `regenerator-runtime` and import them in your entry file.

### 112. How to use HTTPS instead of HTTP in Create React App?
- **Method:** Set the `HTTPS` environment variable to `true` before starting the development server.
  ```bash
  HTTPS=true npm start
  ```

### 113. How to avoid using relative path imports in Create React App?
- **Method:** Use `jsconfig.json` or `tsconfig.json` to configure absolute imports.
  ```json
  {
    "compilerOptions": {
      "baseUrl": "src"
    }
  }
  ```

### 114. How to add Google Analytics for react-router?
- **Method:** Use `react-ga` or similar libraries. Set up Google Analytics tracking within route changes.
  ```jsx
  import ReactGA from 'react-ga';
  import { useLocation } from 'react-router-dom';

  function App() {
    const location = useLocation();

    ReactGA.initialize('UA-000000-01');
    ReactGA.pageview(location.pathname + location.search);

    return (
      // your routes here
    );
  }
  ```

### 115. How to update a component every second?
- **Method:** Use `setInterval` within `useEffect` in function components or `componentDidMount` in class components.
  ```jsx
  useEffect(() => {
    const interval = setInterval(() => {
      // update state or perform actions
    }, 1000);

    return () => clearInterval(interval);
  }, []);
  ```

### 116. How do you apply vendor prefixes to inline styles in React?
- **Method:** Use the `style` attribute with camelCase properties. For complex cases, use libraries like `autoprefixer` or `inline-style-prefixer`.
  ```jsx
  const style = { display: 'flex', WebkitBoxShadow: '0px 4px 6px rgba(0,0,0,0.1)' };
  ```

### 117. How to import and export components using React and ES6?
- **Import:**
  ```jsx
  import MyComponent from './MyComponent';
  ```
- **Export:**
  ```jsx
  export default MyComponent;
  ```

### 118. What are the exceptions on React component naming?
- **Exceptions:** Component names must start with a capital letter to be recognized as components by JSX. Lowercase names are treated as HTML elements.

### 119. Why is a component constructor called only once?
- **Reason:** The constructor is called only when the component is instantiated, not on subsequent re-renders. It’s used for initial setup.

### 120. How to define constants in React?
- **Example:**
  ```jsx
  const API_URL = 'https://api.example.com';
  ```

### 121. How to programmatically trigger a click event in React?
- **Method:** Use `ref` to access the DOM element and then call `click()` on it.
  ```jsx
  const buttonRef = useRef(null);

  useEffect(() => {
    buttonRef.current.click();
  }, []);

  return <button ref={buttonRef}>Click me</button>;
  ```

### 122. Is it possible to use async/await in plain React?
- **Yes:** You can use async/await within event handlers or `useEffect` hooks for asynchronous operations.
  ```jsx
  useEffect(() => {
    const fetchData = async () => {
      const response = await fetch('https://api.example.com');
      const data = await response.json();
      // handle data
    };

    fetchData();
  }, []);
  ```

### 123. What are the common folder structures for React?
- **Example Structure:**
  ```
  src/
  ├── components/
  ├── pages/
  ├── hooks/
  ├── context/
  ├── services/
  ├── utils/
  ├── App.js
  └── index.js
  ```

### 124. What are the popular packages for animation?
- **Packages:**
  - `react-spring`
  - `framer-motion`
  - `react-transition-group`

### 125. What is the benefit of style modules?
- **Benefit:** Scoped CSS that avoids class name collisions by generating unique class names, thus providing modular and reusable styles.

### 126. What are the popular React-specific linters?
- **Linters:**
  - `eslint-plugin-react`
  - `eslint-plugin-jsx-a11y`
  - `eslint-plugin-react-hooks`

### 127. How to make an AJAX call and in which component lifecycle methods should I make an AJAX call?
- **Method:** Use `fetch` or `axios` in lifecycle methods or hooks.
  - **Class Component:** `componentDidMount`
  - **Function Component:** `useEffect`
  ```jsx
  useEffect(() => {
    fetch('https://api.example.com')
      .then(response => response.json())
      .then(data => setData(data));
  }, []);
  ```

### 128. What are render props?
- **Definition:** Render props is a pattern for sharing code between components using a function as a prop.

  **Example:**
  ```jsx
  function DataProvider({ render }) {
    const [data, setData] = React.useState(null);

    React.useEffect(() => {
      // fetch data
      setData(fetchedData);
    }, []);

    return render(data);
  }

  function MyComponent() {
    return (
      <DataProvider render={data => (
        <div>{data ? `Data: ${data}` : 'Loading...'}</div>
      )} />
    );
  }
  ```

### React Router

### 129. What is React Router?
- **Definition:** A library for managing routing in React applications, allowing for dynamic navigation and URL handling.

### 130. How React Router is different from the history library?
- **Difference:** React Router uses `history` to handle URL changes but adds higher-level routing components and features.

### 131. What are the `<Router>` components of React Router v4?
- **Components:**
  - `BrowserRouter`
  - `HashRouter`
  - `MemoryRouter`
  - `StaticRouter`

### 132. What is the purpose of `push` and `replace` methods of history?
- **`push`:** Adds a new entry to the history stack.
- **`replace`:** Replaces the current entry in the history stack.

### 133. How do you programmatically navigate using React Router v4?
- **Method:** Use the `history` object, available from `withRouter` or the `useHistory` hook.
  ```jsx
  import { useHistory } from 'react-router-dom';

  function MyComponent() {
    const history = useHistory();
    const navigate = () => history.push('/new-path');
    return <button onClick={navigate}>Go</button>;
  }
  ```

### 134. How to get query parameters in React Router v4?
- **Method:** Use the `useLocation` hook.
  ```jsx
  import { useLocation } from 'react-router-dom';

  function MyComponent() {
    const location = useLocation();
    const query = new URLSearchParams(location.search);
    const param = query.get('param');
    return <div>Param: {param}</div>;
  }
  ```

### 135. Why you get "Router may have only one child element" warning?
- **Reason:** React Router requires a single child element to manage routing. You can wrap multiple elements in a `<div>` or `<Fragment>`.

### 136. How to pass params to `history.push` method in React Router v4?
- **Example:**
  ```jsx
  history.push(`/path/${param}`);
  ```

### 137. How to implement a default or NotFound page?
- **Method:** Use the `<Route>` with `path="*"` to catch all unmatched routes.
  ```jsx
  <Route path="*" component={NotFoundPage} />
  ```

### 138. How to get history on React Router v4?
- **Method:** Use the `withRouter` higher-order component or `useHistory` hook.
  ```jsx
  import { withRouter } from 'react-router-dom';

  function MyComponent({ history }) {
    // use history object
  }

  export default withRouter(MyComponent);
  ```

### 139. How to perform automatic redirect after login?
- **Method:** Use `history.push` or `useHistory` hook to redirect after successful login.
  ```jsx
  const history = useHistory();
  const handleLogin = () => {
    // Perform login
    history.push('/dashboard');
  };
  ```

### React Internationalization

### 140. What is React-Intl?
- **Definition:** A library for internationalizing React applications, providing components and APIs to format dates, numbers, and messages.

### 141. What are the main features of React Intl?
- **Features:**
  - Formatted messages
  - Date and time formatting
  - Number formatting
  - Pluralization

### 142. What are the two ways of formatting in React Intl?
- **Methods:**
  - **FormattedMessage component**
  - **Intl.formatMessage API**

### 143. How to use `FormattedMessage` as a placeholder using React Intl?
- **Example:**
  ```jsx
  import { FormattedMessage } from 'react-intl';

  function MyComponent() {
    return <input placeholder={<FormattedMessage id="placeholder.text" />} />;
  }
  ```

### 144. How to access current locale with React Intl?
- **Method:** Use the `useIntl` hook to access the `intl` object, which contains the current locale.
  ```jsx
  import { useIntl } from 'react-intl';

  function MyComponent() {
    const { locale } = useIntl();
    return <div>Current locale: {locale}</div>;
  }
  ```

### 145. How to format date using React Intl?
- **Example:**
  ```jsx
  import { FormattedDate } from 'react-intl';

  function MyComponent() {
    return <FormattedDate value={new Date()} year="numeric" month="long" day="numeric" />;
  }
  ```

### React Testing

### 146. What is Shallow Renderer in React testing?
- **Definition:** A utility from `react-test-renderer` to render a component shallowly (i.e., only one level deep) for testing purposes.

### 147. What is TestRenderer package in React?
- **Definition:** Part of `react-test-renderer`, used to render components to a JSON format for snapshot testing.

### 148. What is the purpose of ReactTestUtils package?
- **Purpose:** Provides utilities for testing React components, such as simulating events and rendering components.

### 149. What is Jest?
- **Definition:** A JavaScript testing framework developed by Facebook, used for running tests and providing an easy-to-use API.

### 150. What are the advantages of Jest over Jasmine?
- **Advantages:**
  - Integrated test runner and assertion library
  - Snapshot testing support
  - Built-in mocking capabilities

### 151. Give a simple example of a Jest test case.**
- **Example:**
  ```jsx
  test('adds 1 + 2 to equal 3', () => {
    expect(1 + 2).toBe(3);
  });
  ```

### React Redux

### 152. What is Flux?
- **Definition:** An architecture pattern for managing application state, using unidirectional data flow and actions to update the state.

### 153. What is Redux?
- **Definition:** A state management library for JavaScript applications that follows the Flux architecture, with a single source of truth and pure reducers.

### 154. What are the core principles of Redux?
- **Principles:**
  - **Single Source of Truth:** The state of the entire application is stored in a single object.
  - **State is Read-Only:** The only way to change the state is by dispatching actions.
  - **Changes are Made with Pure Functions:** To specify how the state changes, you write pure reducers.

### 155. What are the downsides of Redux compared to Flux?
- **Downsides:**
  - **Boilerplate:** Redux requires more boilerplate code compared to Flux.
  - **Learning Curve:** The concepts can be more complex for beginners.

### 156. What is the difference between `mapStateToProps()` and `mapDispatchToProps()`?
- **`mapStateToProps`:** Maps state from the Redux store to component props.
  ```jsx
  const mapStateToProps = state => ({
    items: state.items
  });
  ```
- **`mapDispatchToProps`:** Maps dispatch functions to component props.
  ```jsx
  const mapDispatchToProps = dispatch => ({
    addItem: item => dispatch({ type: 'ADD_ITEM', item })
  });
  ```

### 157. Can I dispatch an action in a reducer?
- **No:** Actions should be dispatched in components or middleware, not within reducers. Reducers should be pure functions and only handle state transformations.

### 158. How to access Redux store outside a component?
- **Method:** Use the `store` instance directly if needed, or connect the component to the store via `connect` from `react-redux`.

### 159. What are the drawbacks of the MVW pattern?
- **Drawbacks:** MVW can become complex and less maintainable compared to more modern patterns like MVVM or using state management libraries like Redux.

### 160. Are there any similarities between Redux and RxJS?
- **Similarities:** Both manage state and handle asynchronous operations, though Redux focuses on state management with actions and reducers, while RxJS uses observables and operators.

### 161. How to dispatch an action on load?
- **Method:** Dispatch actions in `componentDidMount` for class components or `useEffect` for function components.
  ```jsx
  useEffect(() => {
    dispatch(fetchData());
  }, [dispatch]);
  ```

### 162. How to use `connect` from React Redux?
- **Method:** Use `connect` to bind Redux state and dispatch to component props.
  ```jsx
  import { connect } from 'react-redux';

  function MyComponent({ items, addItem }) {
    // component implementation
  }

  const mapStateToProps = state => ({
    items: state.items
  });

  const mapDispatchToProps = dispatch => ({
    addItem: item => dispatch({ type: 'ADD_ITEM', item })
  });

  export default connect(mapStateToProps, mapDispatchToProps)(MyComponent);
  ```

### 163. How to reset state in Redux?
- **Method:** Dispatch an action that sets the state to its initial value, handled by the reducer.
  ```jsx
  const initialState = { ... };

  function reducer(state = initialState, action) {
    switch (action.type) {
      case 'RESET_STATE':
        return initialState;
      // other cases
    }
  }
  ```

### 164. What’s the purpose of the `@` symbol in the Redux `connect` decorator?
- **Purpose:** The `@` symbol is not used in Redux or `connect`. It might be a misunderstanding or confusion with decorators in other contexts.

### 165. What is the difference between React context and React Redux?
- **React Context:** Provides a way to pass data through the component tree without manually passing props.
- **Redux:** A state management library that provides a more structured and predictable way to manage global state with actions and reducers

.

### 166. Why are Redux state functions called reducers?
- **Reason:** Reducers are functions that take the current state and an action, and return a new state. The term "reducer" comes from functional programming, where such functions are used to reduce a list of values into a single value.

### 167. How to make AJAX requests in Redux?
- **Method:** Use middleware like `redux-thunk` or `redux-saga` to handle asynchronous operations and dispatch actions based on the request results.

### 168. Should I keep all component's state in Redux store?
- **Recommendation:** Only keep global or shared state in Redux. Local state that is only used within a single component should be managed using React's `useState` or `useReducer`.

### 169. What is the proper way to access the Redux store?
- **Method:** Use the `useSelector` hook to access the store state and `useDispatch` to dispatch actions in function components, or `connect` in class components.

### 170. What is the difference between a component and a container in React Redux?
- **Component:** Typically a presentational component that only receives props and displays data.
- **Container:** A component that connects to the Redux store and dispatches actions. It often contains logic and state.

### 171. What is the purpose of constants in Redux?
- **Purpose:** To avoid typos and ensure consistency when referring to action types. Constants represent action types in a single location.

### 172. What are the different ways to write `mapDispatchToProps()`?
- **Ways:**
  - **Object Syntax:**
    ```jsx
    const mapDispatchToProps = {
      addItem: item => ({ type: 'ADD_ITEM', item })
    };
    ```
  - **Function Syntax:**
    ```jsx
    const mapDispatchToProps = dispatch => ({
      addItem: item => dispatch({ type: 'ADD_ITEM', item })
    });
    ```

### 173. What is the use of the `ownProps` parameter in `mapStateToProps()` and `mapDispatchToProps()`?
- **Purpose:** Provides access to the props that were passed to the component, allowing you to derive new props based on them.

### 174. How to structure Redux top-level directories?
- **Example Structure:**
  ```
  src/
  ├── actions/
  ├── reducers/
  ├── store/
  ├── types/
  ├── middlewares/
  └── selectors/
  ```

### 175. What is redux-saga?
- **Definition:** A middleware library for managing side effects in Redux applications using generator functions.

### 176. What is the mental model of redux-saga?
- **Model:** Think of sagas as long-running processes that listen for dispatched actions and perform asynchronous operations before dispatching new actions.

### 177. What are the differences between `call` and `put` in redux-saga?
- **`call`:** Used to invoke functions or promises.
- **`put`:** Dispatches actions to the Redux store.

### 178. What is Redux Thunk?
- **Definition:** A middleware for handling asynchronous actions in Redux, allowing action creators to return functions instead of actions.

### 179. What are the differences between redux-saga and redux-thunk?
- **`redux-saga`:** Uses generator functions for handling complex side effects and control flow.
- **`redux-thunk`:** Uses simple functions and provides a straightforward way to handle asynchronous actions.

### 180. What is Redux DevTools?
- **Definition:** A set of tools for debugging Redux applications, providing features like time-travel debugging and state inspection.

### 181. What are the features of Redux DevTools?
- **Features:**
  - Time-travel debugging
  - Action and state inspection
  - State and action history

### 182. What are Redux selectors and why use them?
- **Definition:** Functions that extract and compute derived data from the Redux store. They help optimize performance by memoizing results and reducing unnecessary re-renders.

### 183. What is Redux Form?
- **Definition:** A library for managing form state in Redux, providing components and utilities to handle form input, validation, and submission.

### 184. What are the main features of Redux Form?
- **Features:**
  - Form state management
  - Validation and error handling
  - Field-level and form-level validation

### 185. How to add multiple middlewares to Redux?
- **Method:** Use `applyMiddleware` from Redux to add multiple middlewares.
  ```jsx
  import { createStore, applyMiddleware } from 'redux';
  import thunk from 'redux-thunk';
  import saga from 'redux-saga';

  const store = createStore(
    rootReducer,
    applyMiddleware(thunk, saga)
  );
  ```

### 186. How to set initial state in Redux?
- **Method:** Define the initial state in the reducer function and use it as the default value.
  ```jsx
  const initialState = { ... };

  function reducer(state = initialState, action) {
    // reducer logic
  }
  ```

### 187. How is Relay different from Redux?
- **Difference:** Relay is a framework for managing GraphQL data and handling data-fetching logic, whereas Redux is a general state management library for JavaScript applications.

### 188. What is an action in Redux?
- **Definition:** An object representing a change or event that should be processed by the reducer. It typically has a `type` and an optional payload.

### React Native

### 188. What is the difference between React Native and React?
- **Difference:** React is for building web applications, while React Native is for building native mobile applications using React.

### 189. How to test React Native apps?
- **Method:** Use tools like `Jest` for unit tests and `react-native-testing-library` for component tests.

### 190. How to do logging in React Native?
- **Method:** Use `console.log()` for basic logging or libraries like `react-native-logs` for more advanced logging features.

### 191. How to debug your React Native?
- **Method:** Use the React Native Debugger or Chrome Developer Tools for debugging. You can also use `console.log()` for basic debugging.

### React Supported Libraries and Integration

### 192. What is reselect and how does it work?
- **Definition:** Reselect is a library for creating memoized selectors in Redux, which helps improve performance by caching results of selector functions.

### 193. What is Flow?
- **Definition:** A static type checker for JavaScript that allows you to add type annotations and catch type errors during development.

### 194. What is the difference between Flow and PropTypes?
- **Difference:**
  - **Flow:** Provides static type checking at development time.
  - **PropTypes:** Provides runtime type checking for React component props.

### 195. How to use Font Awesome icons in React?
- **Method:** Use `react-fontawesome` or `@fortawesome/react-fontawesome` packages.
  ```jsx
  import { FontAwesomeIcon } from '@fortawesome/react-fontawesome';
  import { faCoffee } from '@fortawesome/free-solid-svg-icons';

  function MyComponent() {
    return <FontAwesomeIcon icon={faCoffee} />;
  }
  ```

### 196. What is React DevTools?
- **Definition:** A browser extension for debugging React applications, allowing you to inspect the React component tree and state.

### 197. Why is DevTools not loading in Chrome for local files?
- **Reason:** Chrome extensions have restrictions on local file URLs. To use DevTools, serve your React app via a local server.

### 198. How to use Polymer in React?
- **Method:** Use Polymer components as custom elements and integrate them into React using the `react-to-webcomponent` library.

### 199. What are the advantages of React over Vue.js?
- **Advantages:**
  - Larger ecosystem and community
  - Strong support for enterprise-level applications
  - Better performance optimization in large applications

### 200. What is the difference between React and Angular?
- **Difference:**
  - **React:** A library for building UI components with a focus on flexibility and a virtual DOM.
  - **Angular:** A full-fledged framework providing a complete solution for building web applications, including data binding, dependency injection, and more.

Here are detailed answers to the questions you provided:

### React DevTools

### 201. Why React tab is not showing up in DevTools?
- **Possible Reasons:**
  - **React DevTools not installed:** Ensure the React DevTools extension is installed and enabled in your browser.
  - **Incompatible React version:** Verify that your React version is compatible with the DevTools version.
  - **DevTools not connected:** Ensure your application is running in development mode. React DevTools usually doesn’t work with production builds.

### Styled Components

### 202. What are styled components?
- **Definition:** Styled Components is a library for React and React Native that allows you to use component-level styles with tagged template literals and CSS. It enables writing CSS-in-JS and provides a way to style components using JavaScript.

### 203. Give an example of Styled Components?
- **Example:**
  ```jsx
  import styled from 'styled-components';

  const Button = styled.button`
    background: blue;
    color: white;
    border: none;
    padding: 10px;
    border-radius: 5px;
    
    &:hover {
      background: darkblue;
    }
  `;

  function App() {
    return <Button>Click me</Button>;
  }
  ```

### Relay

### 204. What is Relay?
- **Definition:** Relay is a JavaScript framework developed by Facebook for building data-driven React applications. It works with GraphQL and handles data-fetching, caching, and synchronization automatically.

### TypeScript with Create React App

### 205. How to use TypeScript in create-react-app application?
- **Steps:**
  1. **Create a new TypeScript project:**
     ```bash
     npx create-react-app my-app --template typescript
     ```
  2. **Convert an existing JavaScript project to TypeScript:**
     - Install TypeScript and types:
       ```bash
       npm install typescript @types/node @types/react @types/react-dom @types/jest
       ```
     - Rename files from `.js` to `.tsx`.
     - Add a `tsconfig.json` file if it doesn’t exist.

### Reselect

### 206. What are the main features of reselect library?
- **Features:**
  - **Memoization:** Avoids recomputing results if input values have not changed.
  - **Selector Composition:** Allows combining multiple selectors.
  - **Performance Optimization:** Helps improve performance by caching derived data.

### 207. Give an example of reselect usage?
- **Example:**
  ```jsx
  import { createSelector } from 'reselect';

  const getItems = state => state.items;
  const getFilter = state => state.filter;

  const getVisibleItems = createSelector(
    [getItems, getFilter],
    (items, filter) => items.filter(item => item.includes(filter))
  );

  // Usage
  const mapStateToProps = state => ({
    items: getVisibleItems(state)
  });
  ```

### React ES6 Classes and Redux

### 209. Does the statics object work with ES6 classes in React?
- **Yes:** Static properties and methods can be defined in ES6 classes, and React allows defining static methods on class components, such as `getDerivedStateFromProps`.

### 210. Can Redux only be used with React?
- **No:** Redux is a standalone state management library that can be used with any JavaScript framework or library. It’s commonly used with React due to its integration with React’s component model.

### 211. Do you need to have a particular build tool to use Redux?
- **No:** Redux can be used with any build tool. It’s framework-agnostic and doesn’t require a specific build tool.

### 212. How Redux Form `initialValues` get updated from state?
- **Method:** Redux Form updates `initialValues` when the `initialValues` prop changes. It uses `shouldComponentUpdate` to check for changes and update the form state accordingly.

### React PropTypes

### 213. How React PropTypes allow different types for one prop?
- **Method:** Use `PropTypes.oneOfType` to specify multiple types for a prop.
  ```jsx
  MyComponent.propTypes = {
    value: PropTypes.oneOfType([
      PropTypes.string,
      PropTypes.number
    ])
  };
  ```

### SVGs and Ref Callbacks

### 214. Can I import an SVG file as a React component?
- **Yes:** Using a tool like `@svgr/webpack`, you can import SVG files as React components.
  ```jsx
  import { ReactComponent as MyIcon } from './my-icon.svg';

  function App() {
    return <MyIcon />;
  }
  ```

### 215. Why are inline ref callbacks or functions not recommended?
- **Reason:** Inline ref callbacks can lead to performance issues because they create a new function on every render, causing unnecessary re-renders or performance degradation.

### Render Hijacking and HOC Factory Implementations

### 216. What is render hijacking in React?
- **Definition:** Render hijacking refers to overriding or altering the default rendering behavior of a component. It is often done in higher-order components (HOCs) to inject additional logic or wrap components with additional functionality.

### 217. What are HOC factory implementations?
- **Definition:** Higher-order component (HOC) factory implementations are functions that create HOCs. They take component(s) as arguments and return a new component with additional functionality.

### Passing Numbers and State Management

### 218. How to pass numbers to React component?
- **Method:** Pass numbers as props just like any other data type.
  ```jsx
  function MyComponent({ count }) {
    return <div>Count: {count}</div>;
  }

  function App() {
    return <MyComponent count={5} />;
  }
  ```

### 219. Do I need to keep all my state into Redux? Should I ever use React internal state?
- **Recommendation:** Only keep global or shared state in Redux. Use React's internal state (`useState`, `useReducer`) for local component state.

### Service Workers and React Memo

### 220. What is the purpose of `registerServiceWorker` in React?
- **Purpose:** Registers a service worker to enable offline capabilities and caching for Progressive Web Apps (PWAs). Service workers help cache assets and serve them from the cache, improving performance and offline functionality.

### 221. What is React memo function?
- **Definition:** `React.memo` is a higher-order component that memoizes a component and prevents unnecessary re-renders if the props haven’t changed.

### React Lazy and Performance Optimization

### 222. What is React lazy function?
- **Definition:** `React.lazy` is a function that allows you to dynamically import components and perform code-splitting, loading components only when they are needed.

### 223. How to prevent unnecessary updates using `setState`?
- **Method:** Use functional `setState` updates to ensure you’re working with the latest state, and avoid unnecessary re-renders by using `React.memo` or `PureComponent`.

### JSX Rendering and Component Classes

### 224. How do you render Array, Strings, and Numbers in React 16 Version?
- **Method:** React 16 supports rendering arrays, strings, and numbers directly in JSX.
  ```jsx
  function MyComponent() {
    const items = ['apple', 'banana', 'cherry'];
    return (
      <div>
        {items.map(item => <div key={item}>{item}</div>)}
        <div>{100}</div>
        <div>{'Hello, world!'}</div>
      </div>
    );
  }
  ```

### 225. How to use class field declarations syntax in React classes?
- **Example:**
  ```jsx
  class MyComponent extends React.Component {
    state = {
      count: 0
    };

    handleClick = () => {
      this.setState(prevState => ({ count: prevState.count + 1 }));
    };

    render() {
      return <button onClick={this.handleClick}>{this.state.count}</button>;
    }
  }
  ```

### Hooks and Their Rules

### 226. What are hooks?
- **Definition:** Hooks are functions that let you use state and other React features in functional components. Examples include `useState`, `useEffect`, and `useContext`.

### 227. What are the rules that need to be followed for hooks?
- **Rules:**
  - **Call hooks at the top level:** Don’t call hooks inside loops, conditions, or nested functions.
  - **Call hooks from React functions:** Only call hooks from React functional components or custom hooks.

### 228. How to ensure hooks follow the rules in your project?
- **Method:** Use ESLint rules with the `eslint-plugin-react-hooks` plugin, which enforces the rules of hooks and helps avoid common mistakes.

### Flux vs Redux

### 229. What are the differences between Flux and Redux?
- **Differences:**
  - **Flux:** An architecture pattern with multiple stores and unidirectional data flow.
  - **Redux:** A state management library with a single store and a more strict set of rules and patterns for managing state.

### Error Boundaries and Lifecycle Methods

### 230. What are the benefits of React Router V4?
- **Benefits:**
  - **Declarative Routing:** Uses JSX to define routes, making it more readable.
  - **Dynamic Routing:** Supports route nesting and dynamic routes.
  - **Code Splitting:** Supports lazy loading and code splitting.

### 231. Can you describe the `componentDidCatch` lifecycle method signature?
- **Signature:

**
  ```jsx
  componentDidCatch(error, info) {
    // error: the error that was thrown
    // info: an object with component stack trace
  }
  ```

### 232. In which scenarios do error boundaries not catch errors?
- **Scenarios:**
  - **Event Handlers:** Errors in event handlers don’t get caught by error boundaries.
  - **Asynchronous Code:** Errors in async code (e.g., setTimeout, Promises) are not caught by error boundaries.
  - **Server-Side Rendering:** Errors during server-side rendering may not be caught by error boundaries.

### 233. Why do you not need error boundaries for event handlers?
- **Reason:** Errors in event handlers are not caught by React’s error boundaries. Instead, you should handle errors directly within the event handler.

### 234. What is the difference between try-catch block and error boundaries?
- **Difference:**
  - **try-catch:** Used for handling synchronous errors within a specific code block.
  - **Error Boundaries:** Used for catching errors that occur in the component tree and rendering fallback UI.

### 235. What is the behavior of uncaught errors in React 16?
- **Behavior:** Uncaught errors in React 16 trigger the error boundary, which provides a fallback UI instead of crashing the whole app.

### 236. What is the proper placement for error boundaries?
- **Placement:** Wrap error boundaries around components or sections of your app where you want to handle potential errors and display fallback UI.

### 237. What is the benefit of the component stack trace from error boundary?
- **Benefit:** Provides detailed information about where the error occurred in the component tree, aiding in debugging and fixing issues.

### Component Methods and Props

### 238. What is the required method to be defined for a class component?
- **Method:** The `render` method is required for class components to specify what to render.

### 239. What are the possible return types of the `render` method?
- **Return Types:**
  - **React elements:** JSX or React.createElement calls.
  - **Arrays:** Arrays of React elements.
  - **Strings and Numbers:** Render text content directly.

### 240. What is the main purpose of the constructor?
- **Purpose:** Initializes state and binds methods to the component instance.

### 241. Is it mandatory to define a constructor for React components?
- **No:** You can omit the constructor if you don’t need to initialize state or bind methods. React will handle it.

### 242. What are default props?
- **Definition:** Default props are values assigned to props if they are not provided by the parent component.
  ```jsx
  MyComponent.defaultProps = {
    text: 'Default Text'
  };
  ```

### 243. Why should you not call `setState` in `componentWillUnmount`?
- **Reason:** Calling `setState` in `componentWillUnmount` can lead to unexpected behavior or memory leaks because the component is about to be removed from the DOM.

### 244. What is the purpose of `getDerivedStateFromError`?
- **Purpose:** Provides a way to update state in response to an error, allowing components to render fallback UI.

### 245. What is the method order when a component is re-rendered?
- **Order:**
  1. `render`
  2. `componentDidUpdate` (if applicable)
  3. `getDerivedStateFromProps` (if applicable)

### 246. What are the methods invoked during error handling?
- **Methods:**
  - `getDerivedStateFromError`
  - `componentDidCatch`

### 247. What is the purpose of the `displayName` class property?
- **Purpose:** Provides a name for the component in debugging tools and error messages, useful for identifying components.

### 248. What is the browser support for React applications?
- **Support:** React supports modern browsers and provides polyfills for older versions. However, the latest features may not work in very old browsers without additional polyfills.

### 249. What is the purpose of `unmountComponentAtNode` method?
- **Purpose:** Unmounts a React component from a DOM node, cleaning up and removing the component’s rendered output.

### Code-Splitting and React Features

### 250. What is code-splitting?
- **Definition:** Code-splitting is a technique to split your code into multiple bundles that can be loaded on demand, reducing the initial load time of your application.

### 251. What is the benefit of strict mode?
- **Benefit:** Strict mode helps identify potential problems in your application by running checks and providing warnings about deprecated practices and unsafe lifecycle methods.

### 252. What are Keyed Fragments?
- **Definition:** Keyed Fragments are a way to provide keys to `Fragment` components to help React identify them and optimize rendering.

### 253. Does React support all HTML attributes?
- **No:** React supports most standard HTML attributes but has some differences, such as using `className` instead of `class` and handling attributes like `style` as objects.

### Higher-Order Components and Debugging

### 254. What are the limitations with HOCs?
- **Limitations:**
  - **Props Conflicts:** Can lead to prop name collisions if not managed properly.
  - **Wrapper Hell:** Multiple HOCs can create deeply nested component trees, making debugging harder.
  - **Static Methods:** HOCs do not automatically pass down static methods or properties.

### 255. How to debug forwardRefs in DevTools?
- **Method:** Use the React DevTools to inspect the components and check if `forwardRef` is working correctly. You may need to check the `ref` prop and ensure it is passed down properly.

### Prop Types and Conditional Rendering

### 256. When do component props default to true?
- **Scenario:** This typically happens when you use boolean props with a default value of `true` if the prop is not explicitly provided.

### 257. What is Next.js and major features of it?
- **Definition:** Next.js is a React framework for building server-side rendered (SSR) applications. Major features include:
  - **Automatic Code Splitting**
  - **Server-Side Rendering**
  - **Static Site Generation**
  - **API Routes**
  - **Built-in CSS and Sass support**

### 258. How do you pass an event handler to a component?
- **Method:** Pass the event handler as a prop to the component.
  ```jsx
  function MyComponent({ onClick }) {
    return <button onClick={onClick}>Click me</button>;
  }

  function App() {
    const handleClick = () => {
      alert('Button clicked!');
    };

    return <MyComponent onClick={handleClick} />;
  }
  ```

### 259. Is it good to use arrow functions in render methods?
- **Recommendation:** Avoid using arrow functions in render methods as it creates a new function instance on every render, which can impact performance. Define methods as class properties or outside the render method.

### 260. How to prevent a function from being called multiple times?
- **Method:** Use techniques like debouncing or throttling to limit the number of times a function can be called.
  ```jsx
  import { useCallback } from 'react';
  import debounce from 'lodash.debounce';

  function MyComponent() {
    const handleClick = useCallback(debounce(() => {
      // Handle click
    }, 300), []);

    return <button onClick={handleClick}>Click me</button>;
  }
  ```

### 261. How does JSX prevent Injection Attacks?
- **Method:** JSX escapes values inserted into the DOM to prevent injection attacks. It treats values as strings and does not allow direct insertion of HTML, thus preventing cross-site scripting (XSS) attacks.

### 262. How do you update rendered elements?
- **Method:** Update elements by changing state or props, which will trigger React’s re-rendering process and update the DOM accordingly.

### 263. How do you say that props are read-only?
- **Reason:** Props are immutable within a component. They are passed from parent to child components and cannot be modified directly by the child component.

### 264. How do you say that state updates are merged?
- **Reason:** When using `setState` in a class component, React merges the new state with the existing state, rather than replacing it entirely.

### 265. How do you pass arguments to an event handler?
- **Method:** Use an arrow function or bind method to pass arguments.
  ```jsx
  function MyComponent() {
    const handleClick = (arg) => () => {
      console.log(arg);
    };

    return <button onClick={handleClick('Hello')}>Click me</button>;
  }
  ```

### 266. How to prevent a component from rendering?
- **Method:** Use `shouldComponentUpdate` in class components or `React.memo` in functional components to control rendering.
  ```jsx
  const MyComponent = React.memo((props) => {
    // component code
  });
  ```

### 267. What are the conditions to safely use the index as a key?
- **Conditions:**
  - **Static List:** The list should not change or reorder.
  - **Unique:** Ensure each item is uniquely identified.

### 268. Should keys be globally unique?
- **No:** Keys only need to be unique among sibling elements in the same list, not globally.

### 269. What is the popular choice for form handling?
- **Popular Choices:** Libraries like `Formik` and `React Hook Form` are popular for handling form state and validation in React applications.

### 270. What are the

 advantages of Formik over Redux Form library?
- **Advantages:**
  - **Less Boilerplate:** Formik requires less setup compared to Redux Form.
  - **Simplicity:** Provides a simpler API and better performance.
  - **Less Dependency on Redux:** Formik does not require Redux, making it easier to integrate with other state management solutions.

### 271. Why do you not require to use inheritance?
- **Reason:** React uses composition instead of inheritance. Components can be combined and extended through composition rather than inheritance, promoting better code reuse and maintainability.

### 272. Can I use web components in React application?
- **Yes:** React can integrate with web components using the `react-shadow` library or directly through the custom elements API.

### 273. What is dynamic import?
- **Definition:** Dynamic import allows you to load modules asynchronously at runtime, enabling code-splitting and reducing initial load times.
  ```jsx
  import('module').then(module => {
    // Use module
  });
  ```

### 274. What are loadable components?
- **Definition:** `react-loadable` or `@loadable/component` are libraries that enable dynamic import and code-splitting for React components, allowing you to load components asynchronously.

### 275. What is the suspense component?
- **Definition:** `React.Suspense` is a component that allows you to handle asynchronous rendering. It lets you specify a fallback UI while components are loading.
  ```jsx
  <React.Suspense fallback={<div>Loading...</div>}>
    <MyComponent />
  </React.Suspense>
  ```

### 276. What is route-based code splitting?
- **Definition:** Route-based code splitting loads different parts of your application based on the route, allowing each route to be split into separate bundles that load on demand.

### 277. Give an example on how to use context?
- **Example:**
  ```jsx
  const MyContext = React.createContext();

  function MyProvider({ children }) {
    const [value, setValue] = React.useState('default');
    return (
      <MyContext.Provider value={{ value, setValue }}>
        {children}
      </MyContext.Provider>
    );
  }

  function MyComponent() {
    const context = React.useContext(MyContext);
    return <div>{context.value}</div>;
  }
  ```

### 278. What is the purpose of default value in context?
- **Purpose:** Provides a default value for the context when a component does not have a matching `Provider` above it in the component tree.

### 279. How do you use `contextType`?
- **Method:** Assign `contextType` to a class component to access context values.
  ```jsx
  class MyComponent extends React.Component {
    static contextType = MyContext;

    render() {
      const context = this.context;
      return <div>{context.value}</div>;
    }
  }
  ```

### 280. What is a consumer?
- **Definition:** A Consumer is a component that subscribes to a context and receives its value. It can be used to access context values from within a function component.
  ```jsx
  <MyContext.Consumer>
    {value => <div>{value}</div>}
  </MyContext.Consumer>
  ```

### 281. How do you solve performance corner cases while using context?
- **Method:** Use context sparingly and split contexts to avoid re-rendering large parts of the component tree. Consider memoizing context values and using `React.memo` for components.

### 282. What is the purpose of `forwardRef` in HOCs?
- **Purpose:** `forwardRef` allows you to pass a `ref` through a component to one of its children, enabling access to the underlying DOM node or component instance.

### 283. Is the `ref` argument available for all functions or class components?
- **No:** `ref` is available only for functional components wrapped with `forwardRef` or class components. It is not directly available in regular functional components.

### 284. Why do you need additional care for component libraries while using forward refs?
- **Reason:** Component libraries often use `forwardRef` to pass refs to underlying DOM elements or components. Proper handling ensures refs are correctly forwarded and avoid issues with ref forwarding.

### 285. How to create React class components without ES6?
- **Example:**
  ```jsx
  var MyComponent = React.createClass({
    getInitialState: function() {
      return { count: 0 };
    },
    render: function() {
      return (
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          {this.state.count}
        </button>
      );
    }
  });
  ```

### 286. Is it possible to use React without JSX?
- **Yes:** React can be used without JSX by using `React.createElement` directly to create elements.
  ```jsx
  const element = React.createElement('div', null, 'Hello, world!');
  ```

### 287. What is the diffing algorithm?
- **Definition:** The diffing algorithm is a method used by React to efficiently update the DOM by comparing the previous and next virtual DOM trees and applying the minimal set of changes.

### 288. What are the rules covered by the diffing algorithm?
- **Rules:**
  - **Elements of the same type:** Compare only elements of the same type.
  - **Component keys:** Use keys to identify components and track changes in lists.
  - **Reorder lists:** Detect and handle reordering of list items based on keys.

### 289. When do you need to use refs?
- **Scenarios:**
  - **Accessing DOM elements:** To interact with or measure a DOM node.
  - **Integrating with third-party libraries:** When you need to use a library that requires direct DOM access.
  - **Managing focus, text selection, or animations.**

### 290. Is it necessary that prop must be named as `render` for render props?
- **No:** While `render` is a common convention, you can name the prop anything. The important part is that it is a function that returns React elements.

### 291. What are the problems of using render props with pure components?
- **Problems:**
  - **Re-render issues:** Pure components may re-render if render props change, even if the data doesn’t.
  - **Prop drilling:** Can lead to deeply nested component structures.

### 292. How do you create an HOC using render props?
- **Example:**
  ```jsx
  function withRenderProps(WrappedComponent) {
    return function RenderPropsComponent(props) {
      return <WrappedComponent {...props} render={props.render} />;
    };
  }

  // Usage
  const EnhancedComponent = withRenderProps(MyComponent);
  ```

### 293. What is windowing technique?
- **Definition:** Windowing (or virtualization) is a technique to render only a portion of a large list of items to improve performance, by only rendering the items that are currently visible.

### 294. How do you print falsy values in JSX?
- **Method:** You can print falsy values by ensuring they are explicitly rendered as strings or use conditional rendering.
  ```jsx
  <div>{false || 'Default text'}</div>
  ```

### 295. What is the typical use case of portals?
- **Use Case:** Portals are used to render children into a DOM node that exists outside the hierarchy of the parent component. Common use cases include modals, tooltips, and dropdowns.

### 296. How do you set default value for uncontrolled components?
- **Method:** Use the `defaultValue` attribute for form elements to set initial values for uncontrolled components.
  ```jsx
  <input defaultValue="Initial value" />
  ```

### 297. What is your favorite React stack?
- **Answer:** Preferences vary, but a popular stack includes React with Redux or Zustand for state management, React Router for routing, and Tailwind CSS or styled-components for styling.

### 298. What is the difference between Real DOM and Virtual DOM?
- **Difference:**
  - **Real DOM:** Directly manipulates the actual DOM, which can be slow and inefficient for complex updates.
  - **Virtual DOM:** A lightweight copy of the real DOM that React uses to perform updates efficiently by calculating differences and applying minimal changes.

### 299. How to add Bootstrap to a React application?
- **Method:** Install Bootstrap via npm or use a CDN.
  ```bash
  npm install bootstrap
  ```
  Then, import Bootstrap CSS in your main JavaScript file:
  ```jsx
  import 'bootstrap/dist/css/bootstrap.min.css';
  ```

### 300. Can you list down top websites or applications using React as the front-end framework?
- **Examples:**
  - **Facebook**
  - **Instagram**
  - **Netflix**
  - **Airbnb**
  - **Uber**
  - **Dropbox**

### 301. Is it recommended to use CSS-in-JS technique in React?
- **Recommendation:** It depends on your project needs. CSS-in-JS can provide scoped styles and dynamic styling but can add complexity. Other solutions include CSS modules or styled-components.

### 302. Do I need to rewrite all my class components with hooks?
- **No:** It’s not necessary to rewrite all class components with hooks. Hooks offer an alternative to class components but both approaches are valid.

### 303. How to fetch data with React Hooks?
- **Example using `useEffect`:**
```jsx
  import { useState, useEffect } from 'react';

  function DataFetchingComponent() {
    const [data, setData] = use

State(null);

    useEffect(() => {
      fetch('https://api.example.com/data')
        .then(response => response.json())
        .then(data => setData(data));
    }, []); // Empty dependency array means this effect runs once on mount

    return <div>{data ? data.name : 'Loading...'}</div>;
  }
```
### 304. How to debug React components?
- **Methods:**
  - **React DevTools:** Provides an interface to inspect React component hierarchy and state.
  - **Console Logs:** Use `console.log` to print component state and props.
  - **Breakpoints:** Set breakpoints in your code to inspect runtime behavior.

### 305. What is the advantage of using `React.memo`?
- **Advantage:** `React.memo` is a higher-order component that optimizes performance by memoizing the result and preventing unnecessary re-renders of functional components if props have not changed.

### 306. What are the common patterns for managing state in React?
- **Patterns:**
  - **Local State:** Managed within components using `useState` or `this.state`.
  - **Context API:** For managing state globally in a component tree.
  - **Redux:** For more complex state management needs, using actions and reducers.
  - **Custom Hooks:** Encapsulate stateful logic and reuse it across components.

### 307. What is the purpose of the `key` prop in lists?
- **Purpose:** The `key` prop helps React identify which items have changed, are added, or are removed. It improves the efficiency of updates by enabling React to optimize re-rendering.

### 308. How do you handle side effects in React functional components?
- **Method:** Use the `useEffect` hook to manage side effects like data fetching, subscriptions, or manually changing the DOM.

### 309. How to manage complex forms in React?
- **Methods:**
  - **Formik:** A library that helps with form management and validation.
  - **React Hook Form:** A library for managing form state and validation with less re-rendering.
  - **Custom Hooks:** Create custom hooks to manage form state and validation logic.

### 310. What is the purpose of `useLayoutEffect` hook?
- **Purpose:** Similar to `useEffect`, but it runs synchronously after all DOM mutations. Useful for reading layout from the DOM and synchronously re-rendering.

### 311. How do you handle errors in React components?
- **Method:** Use error boundaries for catching errors in the component tree and displaying fallback UI. Handle errors in event handlers and async functions directly.

### 312. How to optimize React application performance?
- **Techniques:**
  - **Code-Splitting:** Split code into smaller bundles.
  - **Memoization:** Use `React.memo` and `useMemo` to prevent unnecessary re-renders.
  - **Lazy Loading:** Load components only when needed.
  - **Avoid Inline Functions:** Define functions outside of render methods to avoid unnecessary re-renders.
  - **Optimize Context Usage:** Minimize re-renders by optimizing context usage.

### 313. What are controlled components in React?
- **Definition:** Controlled components are form elements whose value is controlled by React state. Changes are handled via state updates.
  ```jsx
  function ControlledInput() {
    const [value, setValue] = React.useState('');

    const handleChange = (e) => setValue(e.target.value);

    return <input value={value} onChange={handleChange} />;
  }
  ```

### 314. What are uncontrolled components in React?
- **Definition:** Uncontrolled components manage their own state internally, and their value is accessed using refs.
  ```jsx
  function UncontrolledInput() {
    const inputRef = React.useRef();

    const handleClick = () => {
      alert(inputRef.current.value);
    };

    return (
      <>
        <input ref={inputRef} />
        <button onClick={handleClick}>Show Value</button>
      </>
    );
  }
  ```

### 315. How to avoid prop drilling in React?
- **Methods:**
  - **Context API:** Use context to pass data through the component tree without passing props explicitly at every level.
  - **Component Composition:** Structure components to avoid deeply nested props.

### 316. What is the purpose of `useCallback` hook?
- **Purpose:** Memoizes callback functions to prevent them from being recreated on every render, which can optimize performance and prevent unnecessary re-renders.

### 317. What is the `useRef` hook used for?
- **Purpose:** Provides a way to access and interact with DOM elements or store mutable values that do not trigger re-renders when changed.

### 318. How do you handle async operations in functional components?
- **Method:** Use the `useEffect` hook for side effects and async operations, and handle promises using `async/await` inside `useEffect`.

### 319. What is the purpose of `useReducer` hook?
- **Purpose:** Manages complex state logic in functional components, similar to `useState` but with a reducer function for updating state based on actions.

### 320. How do you handle CSS-in-JS in a React application?
- **Method:** Use libraries like `styled-components`, `emotion`, or `@mui/styles` to define and manage styles directly within JavaScript files.

### 321. What is the purpose of `useImperativeHandle` hook?
- **Purpose:** Customizes the instance value that is exposed when using `ref` with `forwardRef`, allowing you to expose specific methods or properties to parent components.

### 322. How do you create and use a custom hook?
- **Example:**
  ```jsx
  function useCustomHook() {
    const [value, setValue] = React.useState('');

    const updateValue = (newValue) => {
      setValue(newValue);
    };

    return [value, updateValue];
  }

  function MyComponent() {
    const [value, updateValue] = useCustomHook();

    return <input value={value} onChange={(e) => updateValue(e.target.value)} />;
  }
  ```

### 323. What is the `useContext` hook used for?
- **Purpose:** Provides access to the context value in functional components without needing to use a `Context.Consumer` component.

### 324. How do you optimize rendering performance in React?
- **Techniques:**
  - **Memoization:** Use `React.memo` and `useMemo` to prevent unnecessary re-renders.
  - **Code-Splitting:** Dynamically import components to reduce initial load time.
  - **Virtualization:** Render only visible parts of large lists.

### 325. What is the difference between `useEffect` and `useLayoutEffect`?
- **Difference:**
  - **`useEffect`:** Runs asynchronously after DOM updates.
  - **`useLayoutEffect`:** Runs synchronously after DOM mutations but before painting, useful for reading layout and making DOM changes.

### 326. How to use `React.Suspense` with lazy-loaded components?
- **Example:**
  ```jsx
  const LazyComponent = React.lazy(() => import('./LazyComponent'));

  function App() {
    return (
      <React.Suspense fallback={<div>Loading...</div>}>
        <LazyComponent />
      </React.Suspense>
    );
  }
  ```

### 327. How to handle user authentication in React?
- **Methods:**
  - **State Management:** Use state or context to manage user authentication status.
  - **Protected Routes:** Create protected routes that only render components if the user is authenticated.

### 328. How to integrate a third-party library with React?
- **Method:** Install the library, then import and use it within your React components. Handle any integration or initialization logic as needed.

### 329. What is React’s Concurrent Mode?
- **Definition:** A set of new features that help React apps stay responsive and gracefully adjust to the user’s device capabilities and network conditions. Features include `Suspense` for data fetching and concurrent rendering.

### 330. How to manage side effects in a React application?
- **Method:** Use the `useEffect` hook for handling side effects such as data fetching, subscriptions, or manually changing the DOM.

### 331. How do you use `useMemo` hook?
- **Purpose:** Memoizes the result of a computation to optimize performance by recalculating the value only when its dependencies change.
  ```jsx
  const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
  ```

### 332. How to handle form validation in React?
- **Methods:**
  - **Formik:** A library for handling form state and validation.
  - **React Hook Form:** A library for managing form state and validation with less re-rendering.
  - **Custom Validation Logic:** Implement validation logic within form components.

### 333. What is the purpose of the `useState` hook?
- **Purpose:** Allows you to add state management to functional components by providing state variables and setter functions.

### 334. How to implement pagination in React?
- **Methods:**
  - **State Management:** Use state to manage the current page and fetch data for that page.
  - **Libraries:** Use libraries like `react-paginate` to handle pagination logic and UI.

### 335. How do you handle route changes in a React application?
- **Method:** Use React Router’s hooks and components, such as `useHistory`, `useLocation`, or `Route`, to handle route changes and navigate programmatically.

### 336. What is the purpose of `React.StrictMode`?
- **Purpose:** Helps identify potential problems in

 an application by activating additional checks and warnings for its descendants, such as deprecated lifecycle methods.

### 337. How to implement dynamic imports in React?
- **Method:** Use dynamic `import()` statements within `React.lazy` to load components asynchronously.
  ```jsx
  const LazyComponent = React.lazy(() => import('./LazyComponent'));
  ```

### 338. What is the purpose of `useEffect` hook dependency array?
- **Purpose:** Specifies dependencies that trigger the effect when they change. If the array is empty, the effect runs only once after the initial render.

### 339. How to handle file uploads in a React application?
- **Methods:**
  - **Controlled Input:** Use a file input element to select files and manage the upload process with state.
  - **Libraries:** Use libraries like `react-dropzone` for more advanced file upload functionality.

### 340. How do you implement conditional rendering in React?
- **Methods:**
  - **Ternary Operator:** Use conditional (ternary) operator within JSX.
  - **Logical && Operator:** Use `&&` to conditionally render components.
  - **Conditional Rendering Functions:** Define functions that return different components based on conditions.
