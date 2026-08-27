Custom Web Browser designed for cheating online exams. WPF + WebView2, .NET, Windows.

## What it does

This web browser was built as an entry point into the Evadus eco-system, designed to make academic dishonesty a little more accessible and easier.

It was open-sourced because I no longer intend to add any more features to it, so you guys can have fun with it.

A lot of degenerates are going to just slap a paywall on it, and then try and sell it to people who don't know better.

So please, when you see someone trying to just fork it, add their logo to it and sell a monthly subscription for it, spam comments saying it's a scam and that it's free on Github.

## Requirements

- .NET SDK (set the version your project targets)
- Windows 10 or 11
- WebView2 Runtime — only needed if you build non-self-contained. Already present on Windows 11 and any machine with current Edge.

## Build

Install .NET. That's the only prerequisite.

Machine already has Edge / WebView2:

```
dotnet publish -c release -r win-x64 --self-contained false -p:AssemblyName=YourAppName -o ./publish
```

Machine has no Edge / WebView2:

```
dotnet publish -c release -r win-x64 --self-contained true -p:AssemblyName=YourAppName -o ./publish
```

Self-contained is larger but needs no .NET and no Edge on the target machine.

`-p:AssemblyName=` sets the executable name — set it to whatever you want.

Output lands in `./publish`.

Replace the app name with something else if you intend to cheat an exam with this.

## License

GPL-3.0. See [LICENSE](LICENSE).
