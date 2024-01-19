# Youtube Player for Flutter Example

```dart
YoutubePlayerController _controller;

@override
void initState(){
    _controller = YoutubePlayerController(
        initialVideoId: 'iLnmTe5Q2Qw',
        flags: YoutubePlayerFlags(
            mute: false,
            autoPlay: true,
        ),
    );
    super.initState();
}

@override
Widget build(BuildContext context){
    return YoutubePlayer(
       controller: _controller,
       showVideoProgressIndicator: true,
       videoProgressIndicatorColor: Colors.amber,
       progressColors: ProgressColors(
          playedColor: Colors.amber,
          handleColor: Colors.amberAccent,
       ),
       onReady: () {
          print('Player is ready.');
       },
    );
}
```
