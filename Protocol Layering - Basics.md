# 💚 Protocol Layering - Basics
## 💛 Background
When a protocol exists, the tasks it performs are divided into multiple stages.
It is far more efficient to think of a **large protocol** not as a single monolithic entity, but as **divided into several distinct stages**. Each of these stages into which the protocol is divided is called a `layer`.
## 💛 What is the Protocol Set?
**Protocol Set**

> A set of combinable protocols
It is also referred to as a `Protocol Stack` or `Protocol Suite`.
## 💛 Basic Terms in Protocol Layering

![](https://prod-files-secure.s3.us-west-2.amazonaws.com/e7a75158-b9c4-4d57-84fa-9858bfaefc38/c3006fa0-702b-428b-9b68-f2fc396a5cd8/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466WO2PAZ6V%2F20250928%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250928T225137Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjED8aCXVzLXdlc3QtMiJIMEYCIQDZbNE%2BZ3E5s95hN9%2BrO2r2jx7fAkCXKQjLG4lqg386LAIhAKqmys54GrDbrdvIviN8GlGTX2q5OVoy7e1i5W96U4%2BBKogECMj%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMNjM3NDIzMTgzODA1Igx9KUC5NyBwXkU7pJEq3AOCI1QAqEr31e%2FtYp%2BiIBy1pgaJcWrguwTUskuoi721OR%2FM8btHj7QasTDihc%2FQv6ZBF9XrCg5SatBZ0%2BoyH7t3yedBauVN7gwguSwiH9P7knN5RDu9vR6CA0JjXw3VJRPbFr6kb%2Fuy3OlD4Ino3sax9d7EiwxL6qmB4bswk7crxIKz25N7ZGrk7cKgmPXoWAdwFeFMllpPj1UqjgCMkStFICczujnv5g5PgmkFW9EyWXaNdb5btmHWyCbKvW6sYdBBcltifkdu7FM%2FPM9XE2imSLQb8TZvuaNh9Odq3GIUDYnwTYcvXARX5LdCFUf0Rce5qfWQ1ETg1yHKav3yQzkMYfM0CUg92Mamwet0zc9pmvXfjfMsUnspMMr%2FwYBudPtG2Y%2FkxIJdPeTS38cwSx%2Bq%2BnCPodl3wQui0St9VOpaZ7Fel4w4oOq57i8jl1gXfd0u%2Fy7tfo2IyBKWeWWoWFByjR6YorwtTQBUVgpvZairKvk3RiiXKTc4qj2XZ0p48d02mhDch%2FoX8h1i33UWlxWrnJCc6L%2Fk4Ior92kNmNz0ExuIwUERoLf0zKKnBXmmSwBglc9xXKZHCZdvV2FCVSXvhRRF1twDnDRA50YavHJKN0mG6UwVjoTBjDsRHzCU8ObGBjqkAZT3uXKQYp1IVEHWJT3U1OG%2Fc8r5PnIFGeLxsf%2B1Sx0qFyt4O%2FznW2b07zShQ7HrUXCSopHLIWhplpRdU%2FAzotF92eH3U3NZLOYpYfH4SMCjDELVGv7jWqQlwQT4Wg3n51jp0cSKaNE3B1TgaAdo%2B2A%2B0X82VcDav2OwZ7s%2B5jqsZKFShxfESYdmmSN14YJ0qNInqcbwzjy%2BB5KFcFjZdSpoRjIf&X-Amz-Signature=fbcd3fd59046a5aeabc34e60de792942a880813f748a74047cf06c44dd3af608&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

### 🤍 Service
**Service**

> A job what the layer does.
- A `service` of the nth layer is provided to the (n+1)th layer

- For example,

    - Service of `TCP`: Providing a byte stream function between each nodes
    
    - Service of `Ethernet`: Providing a unicast/multicast/broadcast function between the network groups
    
### 🤍 Protocol
**Protocol**

> An actual implementation of a service
- A `protocol` is a **set of rules** governing the format and meaning of the packets, or messages that are exchanged by the peer entities within a layer

    - For example, if we defined a service `A`,
    
    - A protocol of `A` implements a task to provide service `A`
    
### 🤍 Interface
**Interface**

> What format does that protocol use for input and output?
- For example, an `interface` of the Physical layer is bit stream

## 💛 Protocol Graph
### 🤍 What is a Protocol Graph?
**Protocol Graph**

> We can display a relationship between each protocols by drawing a **protocol graph**

![](https://prod-files-secure.s3.us-west-2.amazonaws.com/e7a75158-b9c4-4d57-84fa-9858bfaefc38/0782ade9-d2f4-4765-a03d-45fb9a398866/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466WO2PAZ6V%2F20250928%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250928T225137Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjED8aCXVzLXdlc3QtMiJIMEYCIQDZbNE%2BZ3E5s95hN9%2BrO2r2jx7fAkCXKQjLG4lqg386LAIhAKqmys54GrDbrdvIviN8GlGTX2q5OVoy7e1i5W96U4%2BBKogECMj%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMNjM3NDIzMTgzODA1Igx9KUC5NyBwXkU7pJEq3AOCI1QAqEr31e%2FtYp%2BiIBy1pgaJcWrguwTUskuoi721OR%2FM8btHj7QasTDihc%2FQv6ZBF9XrCg5SatBZ0%2BoyH7t3yedBauVN7gwguSwiH9P7knN5RDu9vR6CA0JjXw3VJRPbFr6kb%2Fuy3OlD4Ino3sax9d7EiwxL6qmB4bswk7crxIKz25N7ZGrk7cKgmPXoWAdwFeFMllpPj1UqjgCMkStFICczujnv5g5PgmkFW9EyWXaNdb5btmHWyCbKvW6sYdBBcltifkdu7FM%2FPM9XE2imSLQb8TZvuaNh9Odq3GIUDYnwTYcvXARX5LdCFUf0Rce5qfWQ1ETg1yHKav3yQzkMYfM0CUg92Mamwet0zc9pmvXfjfMsUnspMMr%2FwYBudPtG2Y%2FkxIJdPeTS38cwSx%2Bq%2BnCPodl3wQui0St9VOpaZ7Fel4w4oOq57i8jl1gXfd0u%2Fy7tfo2IyBKWeWWoWFByjR6YorwtTQBUVgpvZairKvk3RiiXKTc4qj2XZ0p48d02mhDch%2FoX8h1i33UWlxWrnJCc6L%2Fk4Ior92kNmNz0ExuIwUERoLf0zKKnBXmmSwBglc9xXKZHCZdvV2FCVSXvhRRF1twDnDRA50YavHJKN0mG6UwVjoTBjDsRHzCU8ObGBjqkAZT3uXKQYp1IVEHWJT3U1OG%2Fc8r5PnIFGeLxsf%2B1Sx0qFyt4O%2FznW2b07zShQ7HrUXCSopHLIWhplpRdU%2FAzotF92eH3U3NZLOYpYfH4SMCjDELVGv7jWqQlwQT4Wg3n51jp0cSKaNE3B1TgaAdo%2B2A%2B0X82VcDav2OwZ7s%2B5jqsZKFShxfESYdmmSN14YJ0qNInqcbwzjy%2BB5KFcFjZdSpoRjIf&X-Amz-Signature=0cee66e041c4b1e495a1b1db409f9ecc40310dcda58831e06644d28bfa2908c6&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

## 💛 Protocol Encapsulation
### 🤍 What is a Protocol Encapsulation?
**Protocol Encapsulation**

> Attaching an additional information as a header or trailer when sending a data packet

![](https://prod-files-secure.s3.us-west-2.amazonaws.com/e7a75158-b9c4-4d57-84fa-9858bfaefc38/da603236-fea9-485c-ab3a-8ea173190383/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466WO2PAZ6V%2F20250928%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250928T225137Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjED8aCXVzLXdlc3QtMiJIMEYCIQDZbNE%2BZ3E5s95hN9%2BrO2r2jx7fAkCXKQjLG4lqg386LAIhAKqmys54GrDbrdvIviN8GlGTX2q5OVoy7e1i5W96U4%2BBKogECMj%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMNjM3NDIzMTgzODA1Igx9KUC5NyBwXkU7pJEq3AOCI1QAqEr31e%2FtYp%2BiIBy1pgaJcWrguwTUskuoi721OR%2FM8btHj7QasTDihc%2FQv6ZBF9XrCg5SatBZ0%2BoyH7t3yedBauVN7gwguSwiH9P7knN5RDu9vR6CA0JjXw3VJRPbFr6kb%2Fuy3OlD4Ino3sax9d7EiwxL6qmB4bswk7crxIKz25N7ZGrk7cKgmPXoWAdwFeFMllpPj1UqjgCMkStFICczujnv5g5PgmkFW9EyWXaNdb5btmHWyCbKvW6sYdBBcltifkdu7FM%2FPM9XE2imSLQb8TZvuaNh9Odq3GIUDYnwTYcvXARX5LdCFUf0Rce5qfWQ1ETg1yHKav3yQzkMYfM0CUg92Mamwet0zc9pmvXfjfMsUnspMMr%2FwYBudPtG2Y%2FkxIJdPeTS38cwSx%2Bq%2BnCPodl3wQui0St9VOpaZ7Fel4w4oOq57i8jl1gXfd0u%2Fy7tfo2IyBKWeWWoWFByjR6YorwtTQBUVgpvZairKvk3RiiXKTc4qj2XZ0p48d02mhDch%2FoX8h1i33UWlxWrnJCc6L%2Fk4Ior92kNmNz0ExuIwUERoLf0zKKnBXmmSwBglc9xXKZHCZdvV2FCVSXvhRRF1twDnDRA50YavHJKN0mG6UwVjoTBjDsRHzCU8ObGBjqkAZT3uXKQYp1IVEHWJT3U1OG%2Fc8r5PnIFGeLxsf%2B1Sx0qFyt4O%2FznW2b07zShQ7HrUXCSopHLIWhplpRdU%2FAzotF92eH3U3NZLOYpYfH4SMCjDELVGv7jWqQlwQT4Wg3n51jp0cSKaNE3B1TgaAdo%2B2A%2B0X82VcDav2OwZ7s%2B5jqsZKFShxfESYdmmSN14YJ0qNInqcbwzjy%2BB5KFcFjZdSpoRjIf&X-Amz-Signature=d2d5d39ddef63719c70fce94e6fdd3e7d79d75ccf05036565f8167f7ce6797df&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

As shown in the figure above, when data originating from `Host1` traverses multiple layers to reach a specific layer on `Host2`, **additional protocol headers such as HHP or RPP are appended** before transmission. 
This process of separately attaching such additional headers or trailers is called `protocol encapsulation`. 
**Q. Why are the Header and Trailer used separately?**

> - Because there is information that must be **sent before the data**, and information that must be **sent afterward**.
> 
> - For example, the Ethernet,
> 
>     - Placing the recipient in the `header` allows for faster initial data transmission, even if subsequent information is incomplete
>     
>     - On the other hand, in the case of CRC, it must be placed in the `trailer` because it must be checked after all the data has been transmitted.
>     
>         - CRC:  Checks whether the data arrived correctly
>         
