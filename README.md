DEPRECATED
=========================
  ATTENTION PLEASE, this project was deleted by myself about several years ago, but there's still some forked version, to avoid misleading someoneelse, I forked back and mark it as DEPRECATED. 
  
  Standalone module like AECM in my project is not recommended anymore, for VoIP app on Android, I suggest you to use the whole WebRTC project(including VoiceEngine/VideoEngine/Codecs/P2P and so on), don't use low-level standalone modules(AECM/NS/VAD/AGC) like I did before, cus' low-level modules need you to configure all the parameters by yourself, its a nightmare, and WebRTC VoE(VoiceEngine) already incorporated them all together and worked well.
  
  If you could not use VoE directly by some reason(like you wanna use your own codecs or transport layer), you could implements the interface of VoE with your own things, or you can use the APM(AudioProcessingModule), its a sub system of VoE and only deal with audio stuffs.






webrtc-based-android-aecm
=========================

  Java API for android acoustic echo cancellation.
  
  I already tested and using it on a LAN demo several monthes ago, it worked well most of the time but sometimes with little squeal, I know there must have something todo to make it better.
To make it better
=========================
  1. Maybe I should build the whole VOE and using the C++ interface proveded by apm? I'll try this later. 
  2. The API is a low level one, most of them are just wrappers of native WebRTC aecm interface. We should handle so many things by ourselves, like estimate the echo tail，handle capture/render threads etc. I'm planning to provide a higher level of the API, which can handle those things for us automatically.

TODO List
=========================
  1. Build the apm interface.
  2. Provide a higher level of the API.
  3. Provide a VoIP demo to show how to use this API instead of doing AECM on PCM files.
