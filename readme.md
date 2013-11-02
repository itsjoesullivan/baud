#baud

badass web audio library

The Web Audio API is powerful and daunting; __baud__ tames it, making it something _fun_.

##

####Constructor
```javascript
baud = new Baud()
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

```javascript
baud.channel(0).at(0).addEvent
```
