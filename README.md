# Functional Interface
**Functional Interface** is an interface with a single abstract method.

        public interface Printer {
            void print(String message);
        }

### Built-In Functional Interfaces

* **Consumer**: single argument with no result. (consumes a value)

        void consum(obj);

* **Supplier**: no input and return a value. (supplies a value)

        obj supply();

* **Function**: map a value to a different value.

        obj map(obj);

* **Predicate**: check that an object satifies some criteria. (to filter data)

        boolean test(condition);

