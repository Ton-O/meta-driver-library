## HA-KPN - driver for meta-PLUS
A driver to control the KPN-box used for TV+; controll via HomeAssistant

### REQUIRES
NEEO-meta-Plus (https://github.com/Ton-O/NEEO-Meta-Plus)
Homeassistant

### How to install 
Install driver through metacore found in the same repository as ths driver (or manually)
change content of this driver to include your Homeassistant API-key (change <xyz> into your apikey at Bearer <xyz>)

### Tested 
Using meta-PLUS running in a container

### Why so complex?
The previous version of this driver connexted to the Android device directly and worked like a charm.
Then came Google with it's drive to make things more universal (a.k.a. secure, future-proof, fitting in their Universe etc.)...  Starting from Android V13, the process of pairing devices has become very complex.
It requires signing up with Google services for API-KEYS and previously used generic mlibraries don;t work anymore because of this.

HomeAssistant has done all that hard work and allows us to communicate with the Android devices through it'sown services.
Maybe in the future when things settle down and knowledge on how to interact directly may show up again; for now it's the road I;ve taken to have things working again.
