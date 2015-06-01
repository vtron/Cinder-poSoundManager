# Cinder-poSoundManager

[Potion's](http://potiondesign.com) basic sound management block for [Cinder](http://libcinder.org).

The block consists of a single class, **SoundManager**, that provides basic sound playback control.

## Features

* Play, loop a track created with a datasource or audio buffer
* Stop a track, all sounds, or tracks in a group
* Track pan and gain
* Signal when a sound has finished playing
* Averaged volume when playing multiple tracks

## Samples

* MultipleSounds: plays a looped sound on mouse down and other sounds on key press.

## Getting Started

Play a sound:

```C++
DataSourceRef source = loadAsset("tune.wav");
po::SoundManager::get()->play(source);
```

Stop a looped sound:

```C++
DataSourceRef source = loadAsset("tune.wav");
unsigned int mTrackID = po::SoundManager::get()->play(source, 0, true); // looped

po::SoundManager::get()->stop(mTrackID);
```
