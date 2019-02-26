# Yet another Authenticator fork

Authenticator is a [TOTP](http://en.wikipedia.org/wiki/Time-based_One-time_Password_Algorithm) based two-factor authentication manager for Pebble. It generates **T**ime-based **O**ne-**t**ime **P**assword for any service offering TOTP two-factor authentication including Google, Dropbox, Facebook, Microsoft, GitHub, Linode, etc.

This is a fork of Neal's SDK 2.0 port of IEF's authenticator fork, which is a fork of pokey9000's twostep.

Mostly, it shows three keys per screen.  It also has some layout tweaks (light background, non-centered text), and vibrates by default when the keys rotate.

Option to vibrate when 5 seconds remain until the token renews and another one for new token.

Uses the JS:Configuration to set the timezone and enable vibration (look for the gear icon near Authenticator in the Pebble mobile app).

Adding secrets via JS:Configuration posseses a security risk of your tokens being sent through a remote server.

Will no longer need to set timezone manually once Pebble SDK supports timezone natively.

## Requirements

Running the `pebble` command assumes you have Pebble SDK 2.0 installed configured to compile Pebble apps.  Also works wit the final 4.3 release.

More info on how to set that up found [here](https://developer.getpebble.com/2/getting-started/).

## Configuration

* Copy `configuration-sample.txt` to `configuration.txt` and add your secrets.

## Install

	$ pebble build
	$ pebble install
