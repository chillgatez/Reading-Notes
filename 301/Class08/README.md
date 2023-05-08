# APIs

## API Design Best Practices

1. What does REST stand for?
    - Representational State Transfer. REST is an architectural style for building distributed systems based on hypermedia.

2. REST APIs are designed around a ____.
    - resource; any kind of object, data, or service that can be accessed by the client

3. What is an identifier of a resource? Give an example.
    - a URI (Uniform Resource Identifier). If I place an order on ubereats or something my indetifier would be a the url to my order
    "https://ubereats.com/orders/12345" "orders" is the resource and "12345" is the identifier.

4. What are the most common HTTP verbs?
    - `````GET`````, `````POST`````, `````PUT`````, `````PATCH`````, and `````DELETE````` are some of the most common operations or 'verbs'

5. What should the URIs be based on?
    - URIs should be based on nouns that represent resources.

6. Give an example of a good URI.
    - A good URI is "https://example.com/products/1234-reviews". This URI represents a resource "reviews" related to a product with the identifier "1234".

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
    - A 'chatty' web API is one that requires a large number of small requests to retrieve or modify a resource. This is generally considered a bad thing as it can lead to increased network latency and decreased performance.

8. What status code does a successful `````GET````` request return?
    - A successful `````GET````` request returns a status code of 200 (OK).

9. What status code does an unsuccessful `````GET````` request return?
    - An unsuccessful `````GET````` request returns a status code of 404 (Not Found).

10. What status code does a successful `````POST````` request return?
    - A successful `````POST````` request returns a status code of 201 (Created).

11. What status code does a successful `````DELETE````` request return?
    - A successful `````DELETE````` request returns a status code of 204 (No Content).