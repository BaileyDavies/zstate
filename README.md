# zstate
ZState is used to manage a redis state based on timestamps in an incoming data stream 

ZState implements all standard redis-go calls, updating the underlying data redis data structures. 

It also tracks the time of the key based on the incoming timestamp of the stream and handles TTL based progress through the stream based on a timestamp

This allows the redis TTL pattern to be applied against data derived from a stream, but moves the basis of the TTL from elapsed time to the time past in the timestamp of the message stream
