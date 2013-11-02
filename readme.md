#baud

badass web audio library

The Web Audio API is powerful and daunting; __baud__ tames it, making it something _fun_.

##

####Constructor
```javascript
baud = Baud()
```

####Basics

It can be very simple:
```javascript
baud.play('/songs/title.mp3')
```

Play a sample:
```javascript
baud.play('/songs/title.mp3');
baud.play(sample);
```

####Channels
```javascript
baud.channel(0).at(0).play('/samples/misc/orchestra_hit.wav');
```

```javascript
baud.set('tempo', 120);
baud.set('length', '3m24s');
```

```javascript
baud.channel(0).each(1/4).play('/samples/dr/kick.wav');
```

Use a drum machine:
```javascript
dr = new baud.drumMachine(['/samples/dr/kick.wav', '/samples/dr/snare.wav'])
dr.ready(function() {
  dr.loop([0, null, 1, null]);
});
```

Use an instrument:
```javascript
rhodes = new baud.instrument('itsjoesullivan/rhodes');
rhodes.ready(function() {
});
```

Or audio input:
```javascript
input = baud.channel(0).listen()
baud.play()
baud.channel(0).record()
baud.channel(0).stop()
```

Sends:
```javascript
verb = baud.reverb('/impulse_responses/plate.wav');
baud.send(0).set('effect', verb);
baud.channel(0).send(0, 0.1)
```

Effects:
```javascript
eq = baud.eq();
eq.low.set('gain', 0.2)
baud.channel.effects.push(eq);
```

```javascript
baud.channel(0).at(0).addEvent
```

Visualize:
```javascript
baud.channel(0).visualize(function(gain) { /* no op */ }, 100);
