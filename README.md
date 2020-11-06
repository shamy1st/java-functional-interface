# Functional Interface
**Functional Interface** is an interface with a single abstract method.

        public interface Printer {
            void print(String message);
        }

### [Built-In Functional Interfaces](https://docs.oracle.com/javase/8/docs/api/java/util/function/package-summary.html)

* [Consumer](https://docs.oracle.com/javase/8/docs/api/java/util/function/Consumer.html): single argument with no result. (consumes a value)

        void consum(obj);

* [Supplier](https://docs.oracle.com/javase/8/docs/api/java/util/function/Supplier.html): no input and return a value. (supplies a value)

        obj supply();

* [Function](https://docs.oracle.com/javase/8/docs/api/java/util/function/Function.html): map a value to a different value.

        obj map(obj);

* [Predicate](https://docs.oracle.com/javase/8/docs/api/java/util/function/Predicate.html): check that an object satifies some criteria. (to filter data)

        boolean test(condition);

---

* **Consumer**

        public class Main {
            public static void main(String[] args) {
                List<String> list = List.of("a", "b", "c");
                Consumer<String> print = item -> System.out.println(item + "");
                Consumer<String> printUppercase = item -> System.out.println(item.toUpperCase() + "");
                Consumer<String> printLowercase = item -> System.out.println(item.toLowerCase() + "");

                list.forEach(print.andThen(printUppercase).andThen(printLowercase));
            }
        }

* **Supplier**

        public class Main {
            public static void main(String[] args) {
                Supplier<Double> getRandom = () -> Math.random();
                double random = getRandom.get(); //Lazy evaluation
                System.out.println(random);
            }
        }

* **Function**



* **Predicate**



