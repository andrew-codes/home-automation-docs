# Multi-Room Audio

## Overview

> Will support streaming to **ANY** dumb speaker with normal speaker jacks.

[Snapcast](https://github.com/badaix/snapcast) server, running in a container on the NUC, with clients running on Raspberry Pis. The Pis can then connect to any dumb speaker. To ensure quality audio, I intend on using a Hifiberry sound card with the Pi. I will likely use the [Amp2](https://www.hifiberry.com/shop/boards/hifiberry-amp2/) since it **can also power the speaker**.

### Support for 3.5mm Dumb Speakers

> This will not power the speakers; meaning there will be two power cables; one for the Pi and one for the speaker.

Instead of using the Amp2, I think the [Hifiberry DAC+ ADC](https://www.hifiberry.com/shop/boards/hifiberry-dac-adc/) will work.

## Streaming Audio: Spotify

While Snapcast can play from a media server, such as [Mopidy](https://mopidy.com/), I intend to only use it with Spotify via Spotify Connect. This means I can **play to** an **individual speaker** or **all speakers** with ease. There is an integration for Snapcast and Spotify ([librespot](https://github.com/librespot-org/librespot) is the library).

## Streaming via AirPlay

> This is still experimental for me in knowing the best way to do this.

You can also use an AirPlay audio container service (using [shairport-sync](https://github.com/mikebrady/shairport-sync)) to make every speaker an AirPlay client. Shairport-sync would run on every Pi client. This is helpful if you have people over and they want to listen to something on a speaker that is not Spotify.
