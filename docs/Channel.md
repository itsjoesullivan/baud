#Channel

##Porcelain

###play

```javascript
channel.play( sample )
channel.play()
```

If passed an argument, attempts to play that argument (e.g., plays a sample).

If not passed an argument, process the current event queue.



###at

```javascript
channel.at( position ).play( sample )
```

Schedule an event to happen at position time.



##Plumbing

###events



###processEvent

Delegates

###processPlayEvent
