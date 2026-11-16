# Launcher

그냥 혼자 혹은 친구랑 만들어서 노는 용도의 마인크래프트 서버 런처입니다.

We are developing a small custom launcher for our private Minecraft: Java Edition community server
("Medieval Server", a medieval-themed economy server running Paper).

Purpose of Minecraft API access:
- Let players sign in with their own Microsoft account so the launcher can obtain a Minecraft session,
  verify game ownership, and launch the official game client.
- The launcher downloads official game files from Mojang, applies our recommended memory settings,
  and connects players directly to our server (online-mode=true, only legitimate accounts can join).

How we handle accounts:
- Sign-in uses Microsoft's official OAuth flow (MSAL). The launcher never sees or stores passwords.
- Tokens are stored only locally on the player's PC in the MSAL token cache. Nothing is sent to our own servers.
- We use the Minecraft Services API only for login and profile lookup (username/UUID). No skin changes, no automation.

Scope:
- Free, non-commercial, for our community members only (around [10-30] players).
- Built in C# (.NET) with the open-source CmlLib.Core library.
- Project page: [[GitHub 또는 웹사이트 주소]](https://github.com/amans124134/Launcher/edit/main/README.md)
