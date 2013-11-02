#Visualizer

Visualizing sound is an integral part of editing music. Our ears can only hear along the time domain, but our eyes can process waveforms non-linearly.

##Signature

```javascript
baud.visualize( fn );
baud.visualize( fn, interval );

baud.visualize.waveform( fn );
baud.visualize.waveform( fn, interval );

baud.visualize.frequency( fn );
baud.visualize.frequency( fn, interval );
```

##Examples

```javascript
// Schedule a 4/4 kick
baud.each(1/4).play('/samples/dr/kick.wav');

// Add a "listener" that displays the volume in a .meter element.
baud.visualize.waveform( function( gain ) {
  $(".meter .needle").css({
    width: (gain * 100) + "%"
  });
});

// Kick things off when kick.wav is loaded.
baud.ready(baud.play);
