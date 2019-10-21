# Presence Detection (Home/Not Home)

## Network Presence Detection

This is much more accurate and reliable than using a geo-fence; although the two are not mutually exclusive.

Home/away is determined when registered phones connect or disconnect from my wireless network. I don’t count it as “not home” unless it is disconnected for at least 3 minutes to prevent false positives.

## GPS Presence Detection

- [iCloud integration](https://www.home-assistant.io/integrations/icloud/) (only iPhone, but does not require any additional apps)
- [Home Assistant app](https://www.home-assistant.io/docs/ecosystem/ios/)(only iPhone)
- [OwnTracks integration](https://www.home-assistant.io/integrations/owntracks/) (all phones; requires installing [OwnTracks app](https://owntracks.org/))

I only use network presence detection to determine if I am home or not. However, I do use GPS for other things; such as reminding me and sending a notification to my phone with my shopping list when I am at a grocery store I frequent often.
