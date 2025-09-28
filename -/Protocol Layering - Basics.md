# 💚 Protocol Layering - Basics
## 💛 Background
When a protocol exists, the tasks it performs are divided into multiple stages.
It is far more efficient to think of a **large protocol** not as a single monolithic entity, but as **divided into several distinct stages**. Each of these stages into which the protocol is divided is called a `layer`.
## 💛 What is the Protocol Set?
**Protocol Set**

> A set of combinable protocols
It is also referred to as a `Protocol Stack` or `Protocol Suite`.
## 💛 Basic Terms in Protocol Layering

![](https://prod-files-secure.s3.us-west-2.amazonaws.com/e7a75158-b9c4-4d57-84fa-9858bfaefc38/c3006fa0-702b-428b-9b68-f2fc396a5cd8/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466RDA25RVM%2F20250928%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250928T225311Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjED8aCXVzLXdlc3QtMiJGMEQCIFlFjpt7WVEkjL98SbRUV8mFmhQmXsylBIp1qPx90LZHAiANAtKzimSMPN2cc74lcc3Raab2QW33KbmHOPjYhlYsQCqIBAjI%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIME3whay%2FaS6qrWRGtKtwDJUBUK6wvTfQKyqNH3x3W6e9rRfUxm7XqcKOqTlsi7sNlf%2Ba5sQno%2BYpfXQO1j8Ex5ufeDFKHcvIv%2BPCj2NDO3GlemgLO23pnHgwsPKs048dEJXJVNHVpDq2A3gfbYN1iegaImpvVXPpN0RVfqy5G8yxBpVVN3A1uklByD3NoFaLuP6OTeumCkifYXvl00KeBkg3wPYZQbmvi6RUymbD0e5DaZLEnupRu6KlwU686xc%2FxOYsxPAzmH8oJp2YnxvBBteyGk4yIbLzb7sA%2FVnk4oO1lskWNh9oU1BSoDy3giNEGj8Llb9NOQIFtsPHGJ7OyNyWTV7Xd9b%2F%2F8YpsFQ%2BSgMO7Ul%2BTpKJPB4a1ihbjsK8%2FWFhhwQy0kpIxKEqBpc%2FLTw9s2QXrb9Rb4PKDbU1eAxxeJCgY7IW7hEG5ApV0U6pj16ONnL4CCRMTx%2FeVQiZG2b6OF%2B2tibZlUuCcRv%2Bz24nj9msXOK6atGdxaZtHP9KLpXjN62A1dD%2FwYLVaAvCVHEGncUBnooS0L147GBoIo5UgufBaPRD54jkeg0bdurHbdeOsXjl5hilHAbw4sJj5%2BlKNUEQtPoj2U%2FOZj7i73mbHcf3eKjorQ4m12lYyljzNASHw%2FPx%2FilH0mHMw1u%2FmxgY6pgFpQ7K0lAd2kYgAfamr88T0pxV6Dj5AzlFN8dWdtMJJIvWp87qAe9Hmvv2onal1Ca8z9jOkZN%2FFu4YbawtJfBO0Ghn3WCJzjko%2BFl%2Fvv%2FoF0fJjhfuOrd7%2F9RRjDJJgat%2B9VYHYvrFjGC%2BiK16LB09ZaRQe%2BId1HAV9MrgZnB7WvPiIeV3vUXQfkyf0zbDXEjGf8Wu4V34QGu4kkX%2F%2F8r90sySShrFn&X-Amz-Signature=0e37f94bc630130356f2bbd628d2a69a1ae9a7f22ab2d9d0411cb3337a361d24&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

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

![](https://prod-files-secure.s3.us-west-2.amazonaws.com/e7a75158-b9c4-4d57-84fa-9858bfaefc38/0782ade9-d2f4-4765-a03d-45fb9a398866/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466RDA25RVM%2F20250928%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250928T225311Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjED8aCXVzLXdlc3QtMiJGMEQCIFlFjpt7WVEkjL98SbRUV8mFmhQmXsylBIp1qPx90LZHAiANAtKzimSMPN2cc74lcc3Raab2QW33KbmHOPjYhlYsQCqIBAjI%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIME3whay%2FaS6qrWRGtKtwDJUBUK6wvTfQKyqNH3x3W6e9rRfUxm7XqcKOqTlsi7sNlf%2Ba5sQno%2BYpfXQO1j8Ex5ufeDFKHcvIv%2BPCj2NDO3GlemgLO23pnHgwsPKs048dEJXJVNHVpDq2A3gfbYN1iegaImpvVXPpN0RVfqy5G8yxBpVVN3A1uklByD3NoFaLuP6OTeumCkifYXvl00KeBkg3wPYZQbmvi6RUymbD0e5DaZLEnupRu6KlwU686xc%2FxOYsxPAzmH8oJp2YnxvBBteyGk4yIbLzb7sA%2FVnk4oO1lskWNh9oU1BSoDy3giNEGj8Llb9NOQIFtsPHGJ7OyNyWTV7Xd9b%2F%2F8YpsFQ%2BSgMO7Ul%2BTpKJPB4a1ihbjsK8%2FWFhhwQy0kpIxKEqBpc%2FLTw9s2QXrb9Rb4PKDbU1eAxxeJCgY7IW7hEG5ApV0U6pj16ONnL4CCRMTx%2FeVQiZG2b6OF%2B2tibZlUuCcRv%2Bz24nj9msXOK6atGdxaZtHP9KLpXjN62A1dD%2FwYLVaAvCVHEGncUBnooS0L147GBoIo5UgufBaPRD54jkeg0bdurHbdeOsXjl5hilHAbw4sJj5%2BlKNUEQtPoj2U%2FOZj7i73mbHcf3eKjorQ4m12lYyljzNASHw%2FPx%2FilH0mHMw1u%2FmxgY6pgFpQ7K0lAd2kYgAfamr88T0pxV6Dj5AzlFN8dWdtMJJIvWp87qAe9Hmvv2onal1Ca8z9jOkZN%2FFu4YbawtJfBO0Ghn3WCJzjko%2BFl%2Fvv%2FoF0fJjhfuOrd7%2F9RRjDJJgat%2B9VYHYvrFjGC%2BiK16LB09ZaRQe%2BId1HAV9MrgZnB7WvPiIeV3vUXQfkyf0zbDXEjGf8Wu4V34QGu4kkX%2F%2F8r90sySShrFn&X-Amz-Signature=e81d7f3db6950ea68912b5052648196fced2186b0eee169e3857cd5a8dfc23ce&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

## 💛 Protocol Encapsulation
### 🤍 What is a Protocol Encapsulation?
**Protocol Encapsulation**

> Attaching an additional information as a header or trailer when sending a data packet

![](https://prod-files-secure.s3.us-west-2.amazonaws.com/e7a75158-b9c4-4d57-84fa-9858bfaefc38/da603236-fea9-485c-ab3a-8ea173190383/image.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=ASIAZI2LB466RDA25RVM%2F20250928%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20250928T225311Z&X-Amz-Expires=3600&X-Amz-Security-Token=IQoJb3JpZ2luX2VjED8aCXVzLXdlc3QtMiJGMEQCIFlFjpt7WVEkjL98SbRUV8mFmhQmXsylBIp1qPx90LZHAiANAtKzimSMPN2cc74lcc3Raab2QW33KbmHOPjYhlYsQCqIBAjI%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAAaDDYzNzQyMzE4MzgwNSIME3whay%2FaS6qrWRGtKtwDJUBUK6wvTfQKyqNH3x3W6e9rRfUxm7XqcKOqTlsi7sNlf%2Ba5sQno%2BYpfXQO1j8Ex5ufeDFKHcvIv%2BPCj2NDO3GlemgLO23pnHgwsPKs048dEJXJVNHVpDq2A3gfbYN1iegaImpvVXPpN0RVfqy5G8yxBpVVN3A1uklByD3NoFaLuP6OTeumCkifYXvl00KeBkg3wPYZQbmvi6RUymbD0e5DaZLEnupRu6KlwU686xc%2FxOYsxPAzmH8oJp2YnxvBBteyGk4yIbLzb7sA%2FVnk4oO1lskWNh9oU1BSoDy3giNEGj8Llb9NOQIFtsPHGJ7OyNyWTV7Xd9b%2F%2F8YpsFQ%2BSgMO7Ul%2BTpKJPB4a1ihbjsK8%2FWFhhwQy0kpIxKEqBpc%2FLTw9s2QXrb9Rb4PKDbU1eAxxeJCgY7IW7hEG5ApV0U6pj16ONnL4CCRMTx%2FeVQiZG2b6OF%2B2tibZlUuCcRv%2Bz24nj9msXOK6atGdxaZtHP9KLpXjN62A1dD%2FwYLVaAvCVHEGncUBnooS0L147GBoIo5UgufBaPRD54jkeg0bdurHbdeOsXjl5hilHAbw4sJj5%2BlKNUEQtPoj2U%2FOZj7i73mbHcf3eKjorQ4m12lYyljzNASHw%2FPx%2FilH0mHMw1u%2FmxgY6pgFpQ7K0lAd2kYgAfamr88T0pxV6Dj5AzlFN8dWdtMJJIvWp87qAe9Hmvv2onal1Ca8z9jOkZN%2FFu4YbawtJfBO0Ghn3WCJzjko%2BFl%2Fvv%2FoF0fJjhfuOrd7%2F9RRjDJJgat%2B9VYHYvrFjGC%2BiK16LB09ZaRQe%2BId1HAV9MrgZnB7WvPiIeV3vUXQfkyf0zbDXEjGf8Wu4V34QGu4kkX%2F%2F8r90sySShrFn&X-Amz-Signature=579d8bb346220ad6b175ba02577f6deb464fd39398fd85123e9379a7048252f0&X-Amz-SignedHeaders=host&x-amz-checksum-mode=ENABLED&x-id=GetObject)

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
