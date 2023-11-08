# Push To Talk

A simple javsacript snippet that shows how to make a simple push button voice to text recorder.

```javascript
initializePushToTalk("F10");

document.addEventListener("speech", (event) => {
  const transcript = event.detail;
  const transcriptElement = document.createElement("p");
  transcriptElement.innerText = transcript;
  document.body.appendChild(transcriptElement);
});

document.addEventListener("speechstarted", () => {
  const statusElement = document.createElement("p");
  statusElement.innerText = "Listening...";
  document.body.appendChild(statusElement);
});

document.addEventListener("speechended", () => {
  const statusElement = document.createElement("p");
  statusElement.innerText = "Stopped listening.";
  document.body.appendChild(statusElement);
});
```

See full code and demo [here](https://richardanaya.github.io/push-to-talk/index.html).

LICENSE: MIT
