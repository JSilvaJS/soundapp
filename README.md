# Synopsis
A basic sound player built with HTML, CSS, React.js & SoundCloud API.


# Sample Code
```javascript
playHandler() {
	this.player.play();
	this.updatePosition();
	this.interval = setInterval(::this.updatePosition, 1000);
}

updatePosition() {
	window.player = this.player;
	if (this.player.controller) {	
		this.setState({
			duration: this.player.controller.getDuration(),
			position: this.player.controller.getCurrentPosition()
		});
	}
}

stopHandler() {
	this.player.pause();
	clearInterval(this.interval);
}
```
