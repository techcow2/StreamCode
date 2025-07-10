# StreamCode

Yi 4k Live QR Code Generator

<a href="https://play.google.com/store/apps/details?id=com.streamcode.app">
  <img alt="Get it on Google Play"
       height="80"
       src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png">
</a>

---

## 💡 How It Works

1.  User fills the form → the app builds a JSON object:
    ```
    {
      "ssid": "MyWiFi",
      "pwd" : "hunter2",
      "res" : "1080p",
      "rate": "3",          // mapping: High=3 Medium=2 Low=1 Auto=0
      "dur" : "0",
      "url" : "rtmp://example.com/live/key"
    }
    ```
2.  `qrcodejs` converts that JSON into a **v4-L** QR code (highest error level).
3.  Yi 4 K camera scans the code on the LCD and applies the settings instantly.

---

## 📦 Built With

| Tech              | Purpose                                  |
|-------------------|------------------------------------------|
| **HTML / CSS**    | single-page UI                           |
| **Tailwind 2**    | utility classes (no extra CSS build step)|
| **JavaScript**    | form logic & localStorage CRUD           |
| **qrcodejs**      | QR code generation                       |
| **Lucide**        | crisp SVG icon set                       |

---

## 🌐 Offline Mode

Click **Offline Mode** → the page serialises itself with `document.documentElement.outerHTML`,
wraps it in a Blob and triggers a download (`StreamCode_Offline.html`).
Open that file anywhere – it contains in-lined settings and still references the same public CDNs.

---

## 📝 Roadmap

- [ ] Dark-mode toggle  
- [ ] Custom logo upload  
- [ ] PWA manifest & service-worker for installable experience  
- [ ] Translations (EN · ES · ZH · RU)

---

## 🤝 Contributing

1. Fork the project  
2. Create your feature branch: `git checkout -b feature/amazing`  
3. Commit your changes: `git commit -m 'feat: add amazing feature'`  
4. Push to the branch: `git push origin feature/amazing`  
5. Open a Pull Request

---

## 🔒 License

Distributed under the **MIT** license.  
See [`LICENSE`](LICENSE) for more information.

---

## 🙋‍♂️ Author

**IslandApps** – <https://islandapps.dev>

Feel free to reach out on GitHub issues if you find a bug or have a feature request!
