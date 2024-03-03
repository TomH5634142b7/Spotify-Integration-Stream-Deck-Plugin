# ⚠️ This is far from complete.
This repo is here to show what's to come.

Progress on the Stream Deck plugin currently hasn't started yet as I'm getting the [Spicetify Custom API Extension](https://github.com/TomH5634142b7/Spicetify-Custom-API-Extension) ready first. This plugin will depend on the custom API extension.

# Spotify Integration Stream Deck Plugin
This plugin was built as an alternative to BarRaider's Spotify Integration which uses the Spotify Web API.

This plugin creates a local websocket server which will handle sending and receiving data from my custom webhook API extension for Spicetify.

# Installation

# FAQ
## Why?
The Web API is good, but it has its pitfalls.

You have to always be online and BarRaider's Spotify plugin for the Stream Deck is pretty delayed to avoid Web API rate-limits.

I've also personally had issues with BarRaider's plugin staying connected when you leave Spotify inactive but still open for a bit.

Because of this, I decided to make this extension to go with my own custom Stream Deck plugin.

## Why not use WebNowPlaying?
Using WebNowPlaying was my original goal, but I later realised this may cause compatibility issues with Rainmeter due to the same port (8974) being used for both websocket servers.

Instead of looking for other ways to use WebNowPlaying, I realised I could make something that works for more than just me. A more developer-friendly Spotify websocket API.

## Why send so much data over to the websocket server?
Even though my Stream Deck plugin requires very little data, I can see other projects having a wide variety of use-cases that may benefit from the extra data.

If you plan to make an external websocket server, you can fork this repository and remove any unnecessary data in the app.tsx SendUpdate function to optimise bandwidth usage.

I do get that some of the data (page_instance_id or is_buffering for instance) is probably highly unnecessary, but you never know. My goal for this project is to create a developer-friendly API that just works without that much hassle.
