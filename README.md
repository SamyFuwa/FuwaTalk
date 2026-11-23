# FuwaTalk VR

**English** | [日本語](README.ja.md)

Voice translator and anime-style subtitles for VRChat. The translation runs on your own PC.

- **You → them:** you speak, and your translation appears in your VRChat chatbox. It can also be spoken aloud with a synthetic voice.
- **Them → you:** what people say near you appears as translated subtitles, in your headset or on your screen.

> **For friends only.** This is a personal, non-commercial project. You need a personal key, given by its author, to install it.

## Before you download

- **Languages you can use right now:** English, Spanish and French. Japanese is **not** available yet.
- **The app itself is in Spanish.** In this page, Spanish menu names appear *(in italics)* so you can find them.
- Windows 10 (version 2004) or later, 64-bit.
- An NVIDIA graphics card is recommended. AMD and Intel cards use DirectML, which has not been tested on a real AMD card yet. It also works without a graphics card, but slowly.
- Between about 1 and 7 GB of AI models are downloaded once, depending on the translator you choose.

## Install

1. Open [Releases](../../releases/latest) and download `FuwaTalk-X.Y.Z-instalador.exe`. You do not need the `actualizacion` file: the app uses it to update itself.
2. Open it, paste your key (it starts with `FUWA-`) and answer a few questions:
   - Man or woman: chooses the type of synthetic voice.
   - Age: under 18 turns the swear-word filter on. You can switch it at any time.
   - Your native language, and the language to translate into.
   - Which translator to use. The one recommended for your PC is marked.
   - Whether to install VB-Cable, needed only for the synthetic voice.
3. The first time it opens, the app downloads what you chose.

If it is already installed, opening the installer again lets you update or repair it, change your answers, or uninstall it.

## Set up VRChat (once)

1. Turn on OSC: radial menu → *Options* → *OSC* → *Enabled*.
2. Only if you want others to hear your translation: *Settings* → *Audio* → *Microphone* → **CABLE Output (VB-Audio Virtual Cable)**.

While FuwaTalk is open it also passes your real voice to that cable, unless the synthetic voice is on. **If you close the app, choose your normal microphone in VRChat again**, or nobody will hear you.

## What it can do

### Translate your voice
- Speak normally. When you finish a sentence, the translation is sent to the **chatbox**, with a typing indicator.
- Long texts are split into pages. You can set the prefix, the time per page, the notification sound, and whether to add the original text.
- Choose what you speak *(Yo hablo)* and the target language *(Traducir a)*, and swap them with one button.
- Optional push-to-talk. If you are muted in VRChat, nothing is translated or spoken.

### Synthetic voice (TTS)
- **On:** people in VRChat hear only the synthetic voice speaking your translation.
- **Off:** people hear your real voice, and your translation goes to the chatbox.
- Female and male voices in English and Spanish. French has a female voice only.
- Pick a voice per language and preview it. Adjust speed and volume, and optionally listen to yourself.
- **Review first** *(Revisar antes)*: nothing is spoken until you confirm it.

### Subtitles for other people
- **In VR:** a SteamVR overlay. You can adjust its distance, height, width and how it follows your head.
- **On desktop:** over the VRChat window. By default this is automatic when there is no VR.
- **One person** *(Solo interlocutor)*: subtitles only the person you are talking to. You can lock onto a voice.
- **Conversation** *(Conversación)*: several voices at once, each with its own colour.
- **Who gets subtitles:** a slider from everyone to only the person next to you.
- If someone speaks for a long time, the subtitle appears in parts while they talk.
- Adjustable size, outline, opacity, dark strip, number of lines and time on screen.

VRChat does not share player positions, so closeness is *estimated* from volume, direction and the sound of each voice. It can be wrong, and two people talking at exactly the same time may get mixed.

### Typing mode *(Modo escribir)*
- Type instead of speaking. Your text is translated (or not), spoken, and sent to the chatbox.
- In VR it opens the SteamVR keyboard. On desktop, a small box appears over VRChat.
- It can silence your real microphone while it is on.

### Swear-word filter *(Sin palabrotas)*
- `****` in the chatbox and subtitles, and a beep in the synthetic voice. You can add your own words.
- It does **not** cover your real voice or other people's voices.

### Privacy
- Speech recognition, translation and the synthetic voice run on your PC. Your audio and text are not sent to any translation service.
- The app uses the internet to download models and VB-Cable, and to ask GitHub for new versions and the list of cancelled keys. The translation you send to the chatbox goes to VRChat, as usual.
- **History** is saved only on your PC, for 30 days by default. You can search it, export it, delete it or turn it off.
- **Private mode** *(Modo privado)*: what other people say is not saved to your disk.

### Other features
- **Glossary:** words that are never translated, and your own corrections.
- **Global hotkeys:** they work inside the game and you can change them.
- **SteamVR:** can open with SteamVR and start translating by itself.
- **Pause:** frees the graphics memory. You can turn this off.
- **Updates:** tells you when there is a new version and asks before installing it.

## Hotkeys

| Keys | Action |
|---|---|
| `Ctrl+Alt+T` | Pause / resume |
| `Ctrl+Alt+L` | Lock / unlock the person you are talking to |
| `Ctrl+Alt+Enter` | Speak the pending translation (Review first) |
| `Ctrl+Alt+Space` | Push-to-talk, if you turned it on |
| `Ctrl+Alt+K` | Type a message |

## Which option for your PC

| Option in the app | Graphics memory (NVIDIA) | Model download | Result |
|---|---|---|---|
| *PC sin gráfica* (no graphics card) | None | about 1.3 GB | Works, but slow |
| *PC malo* (basic) | under 1 GB | about 1.3 GB | Very light. Word-for-word, sometimes wrong |
| *PC medio* (medium) | about 3 GB | about 5.3 GB | Natural translation |
| *PC bueno* (powerful) | about 4.5 GB | about 7 GB | The best one: understands jokes and expressions better |

If the game stutters, choose a lower one in *Ajustes* (Settings).

## If something goes wrong

| Problem | Try this |
|---|---|
| Nothing in the chatbox | Turn on OSC in VRChat and send a test message from the *Chatbox* page |
| Others cannot hear the synthetic voice | VRChat's microphone must be `CABLE Output`, and *Voz TTS* must be on |
| Others cannot hear you | Keep FuwaTalk open, or go back to your normal microphone |
| No subtitles in VR | Open SteamVR and check *Subtítulos → En el visor* |
| No subtitles on desktop | Set *Subtítulos → En la pantalla* to *Siempre*, and use a windowed or borderless game |
| It translates noise or distant voices | Move the subtitles slider to the right |
| Sentences are cut too early | Raise *Ajustes → Silencio para cerrar frase* |

Automatic translation makes mistakes. Do not rely on it for anything important.

## Credits

Built with Whisper (faster-whisper), NLLB-200, Gemma, Kokoro, eSpeak NG, llama.cpp, PySide6 (Qt) and VB-CABLE. Each one belongs to its authors and has its own licence.

FuwaTalk is an unofficial project. It is not affiliated with or endorsed by VRChat, Valve, VB-Audio or the projects above.
