# Steganography Toolset : WAV Encoder/Decoder

## To build 
Use provided Makefile

## Usage
./wavcodec encode <input.wav> <message> <output.wav>
OR      ./wavcodec decode <input.wav> <output>

## Demo
I discuss a simple test of this utility on my portfolio website, here's a link to that page: [Audio Steganography](http://10.0.0.22/Steganography)
## Description 
Given a input wave file of sufficient size, a binary file <message> can be encoded into the bits of the input file, producing an output wave file, 
which has the exact size, properties and playback capabilties as the original file, within which <message> is encoded as noise which is hard to
detect by a human. 

The codec doesn't require the original file to decode, hence the original can be safely destroyed without compromising the integrity of the payload.

Depending on the size of message and ballast file, the program can determine how many bits to use in order to try and maintain the noise introduced 
to be minimum.

The provided source code can be altered with relative ease for multithreaded perfomance, as the problem at hand is embarrasingly parrallel.

This module is part of *CS241 Honors (CS296-41) Project: Steganography Toolset* which I helped in creating along with my two team members
[Dan Johnson](https://github.com/dsjohns2) and [Anton Bershianskiy](https://github.com/bershan2). The orginal project can be found at this [link](https://github.com/dsjohns2/CS-241-Honors-Project).
