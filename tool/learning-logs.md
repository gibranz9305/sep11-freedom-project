# Tool Learning Log

## Tool: **Howler**

## Project: Alarm that makes you solve math problems before it turns off, good for reminders 

---

### 10/24/26:
## Howler

Howler is used for audio in JS, it would work well for my freedom project idea, as a way to add alarm sounds/


The examples in the documentation included audio in video games and live radios, as well as music players.

Here are some examples of howler in the website [1](https://howlerjs.com/#player)
[2](https://howlerjs.com/#radio)

## How to install
To install howler, I need to clone the repo [here](https://github.com/goldfire/howler.js#examples). And install it with either _npm_, _yarn_, or _bower_ but I do not know what these are. 

```js
<script src="/path/to/howler.js"></script>
<script>
    var sound = new Howl({
      src: ['sound.webm', 'sound.mp3']
    });
</script>
```
This was some example code, after installing you use `<script src="/path/to/howler.js"></script>`, in order for you to actualy use it.

# Examples
```js
var sound = new Howl({
  src: ['sound.mp3']
});

sound.play();
```
This code plays any mp3. It is very simple. In order to playback audios. You would use ` autoplay: true,` alongisde the audio you want to be replayed. In the github repo, this is the example given
```js
var sound = new Howl({
  src: ['sound.webm', 'sound.mp3', 'sound.wav'],
  autoplay: true,
  loop: true,
  volume: 0.5,
  onend: function() {
    console.log('Finished!');
  }
});
```
This code woud playback between *sound.webm*, _sound.mp3_, and _sound.wav_.
`volume` is also a way to change the volume without using your own devices volume.

# Important information
Setting `loop Boolean false` to `true` will continously play an audio.

`mute Boolean false` When set to true the audio will be muted.

`rate Number 1.0` Playback speed of audios, can be changed 

`onloaderror Function`. If the sound cannot be played, this give an error message. 




### 11/7/26:
* Howler tinkers
`<script src="https://cdnjs.cloudflare.com/ajax/libs/howler/2.2.4/howler.min.js"></script>`
Is needed for the project and tinkering.

I donwloaded the sound for the tinkering from [here](https://freesound.org/people/zanox/sounds/233645/) freesound.

I had to make 2 new folders, _public_ and _audio_, and i put the audio in the audio folder.

I added the donwloaded sound as `const alarm = new Howl({ src: ['/audio/alarm.wav'] });` which will allow for *howler.js to use it*

`.addEventListener('click', () => {
    alarm.play();`

This is the hwoler code I used to make it so when i click something it will play the alarm sound that i donwloaded. I made a button id and used documetn query selector.

Now the audio plays when I click the bytton, but i also still need to add the math problems and a button to stop the sound. I want the math problems to also pop up as the sound is playing, and for the sound to turn off when they are done. 

Before the button I also want to add a selector where you pick what thing you need to get done, and pick a start and end date.


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
