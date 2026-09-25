# Mic Gain Check

A one-page microphone level meter: [open the live site](https://bioshazard.github.io/mic-gain/).

Click **Start listening**, allow microphone access, and speak at your normal distance. Try your loudest expected phrase. Adjust your microphone, audio interface, or system input gain until the loudest peaks are roughly **−12 to −6 dBFS**. The page shows a ten-second peak and average graph, recent maximum, and near-ceiling hits.

Everything runs in your browser. The page does not record, upload, or play your microphone audio, and it has no runtime dependencies. It requests automatic gain control, echo cancellation, and noise suppression off where the browser supports those controls. A microphone or preamp can distort before the digital signal reaches 0 dBFS.

To run locally, open `index.html` in a browser. If microphone access is blocked for local files, serve this directory on localhost:

```sh
python3 -m http.server 8765 --bind 127.0.0.1
```

Then open <http://127.0.0.1:8765/>.

The peak target follows [Audacity's recording-level guidance](https://manual.audacityteam.org/man/faq_recording_how_to_s.html), which recommends a maximum peak around −6 dBFS.
