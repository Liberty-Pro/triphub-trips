# Trip Hub trips

Encrypted trip files for the [Trip Hub](https://play.google.com/store/apps/details?id=com.libertyindicators.triphub)
Android app, served by GitHub Pages at https://liberty-pro.github.io/triphub-trips/.

- `t/*.bin` are trip files encrypted with AES-256-GCM. Each has its own random key, which exists only in the
  trip's QR code and link (after the `#`, the part a browser never sends to a server). Without that key the
  files are unreadable, and their random names say nothing about whose trip they are.
- `index.html` is the page a phone's camera opens when it scans a trip code. It reads the code from the link
  and hands it to the Trip Hub app on the phone. It sends nothing anywhere and has no analytics.

Files are added and removed by the publishing script in the (private) Trip Hub repo; nothing here is edited
by hand. Every file must start with the `THX1` header: plain trip files never belong here.
