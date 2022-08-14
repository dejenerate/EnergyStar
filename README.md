# EnergyStar

EnergyStar is a terrible* Windows application that leverages [Windows EcoQoS API](https://devblogs.microsoft.com/performance-diagnostics/introducing-ecoqos/) to throttle any inactive user process and background applications to improve system thermal and battery life, similar to the process management strategy on modern Apple macOS releases.

## See It In Action

![Battery stat on Z13](https://pbs.twimg.com/media/FY5oAiFVQAAlR5d?format=png&name=medium)

*: By saying _terrible_, I mean currently there are a few known limitations on track to be addressed. See below.

EnergyStar runs in a terminal window and boosts or throttles applications based on which one is active and which ones are idle.

[See it in action](https://replayable.io/replay/62f95b3f8716cc0062b9dfc8)

## Known Limitations

* Child processes do not get boosted when the parent process receives input focus.
* Throttle is always engaged regardless of power scheme and power source.
* System processes (which is Session 0) do not get throttled. Currently there are some assumption that non-user processes know what they are doing.
* Process exemption list is not user configurable.

## Usage

Download the release binary and double click `EnergyStar.exe`

For development, standard .NET 6 toolchains are required. The project structure should be self-explanatory.

## License

Dual licensed: MIT License with Microsoft exemptions.
