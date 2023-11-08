# Push To Talk

A simple javsacript snippet that shows how to make a simple push button voice to text recorder.

```
initializePushToTalk("F10");

document.addEventListener("speech", (event) => {
    const transcript = event.detail;
    const transcriptElement = document.createElement("p");
    transcriptElement.innerText = transcript;
    document.body.appendChild(transcriptElement);
});
```