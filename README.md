# HolySoundManager
Better and Easier Sound Management Library for Unity

# How to Set up
Just Drag and Drop the HolySoundManager file into unity.

# Example
using Holylib.HolySoundEffects;

public AudioClip clip;

// play any audio clip as sfx
SoundEffectController.PlaySFX(clip);

// play any audio clip as music
SoundEffectController.PlayMusic(clip);

// play any audio clip and hold the source
var audioObject = SoundEffectController.PlaySFX(clip);

// stop any audio clip
audioObject.StopSFX();

// stop all audio clips
SoundEffectController.StopAllSounds();

// change volume
SoundEffectController.MasterVolume = 0.5f;
SoundEffectController.MusicVolume = 0.5f;
SoundEffectController.SFXVolume = 0.5f;

// change the parameters of a clip
SoundEffectController.PlaySFX(clip)
.SetLoop(True)
.SetVolume(0.5f)
.RandomPitchRange(-0.5f,0.6f)
.SetPitch(0.5f)
.SetDontDestroyOnLoad();
