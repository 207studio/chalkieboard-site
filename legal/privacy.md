---
title: Privacy Policy — Chalkieboard
permalink: /legal/privacy/
---

<script>(function(){try{var q=new URLSearchParams(location.search);if(q.get("lang")==="en"){localStorage.setItem("chalkieboard.lang","en");return}if(localStorage.getItem("chalkieboard.lang")==="en")return;var l=(navigator.languages&&navigator.languages[0])||navigator.language||"";if(/^ko(\b|-|_)/i.test(l))location.replace("/ko"+location.pathname+location.hash)}catch(e){}})();</script>

# Privacy Policy — Chalkieboard

한국어: [개인정보처리방침](/ko/legal/privacy/)

**Effective date: November 16, 2026**

Chalkieboard is an iPad tool for teachers and presenters. It does not provide student
accounts or ask teachers to register student identities. Lesson materials, handwriting
and spoken commands can still contain personal information. This policy explains local
processing and the optional sharing described below.

---

## 1. Summary

**Chalkieboard does not send your lesson files, board images or timetable to the developer's
servers.** They are kept on your device and, when you choose to use it, in your own iCloud.
The developer cannot access them.

**The version with a Use Decisions setting keeps Decisions off by default.** The app uses
Apple's on-device speech recognition and local rules for supported commands. Only after
new consent and a separately entered OpenAI voice key may selected command text and screen
context go to OpenAI (Section 5.2). Existing TypeSafe keys and consent are unused.

Build `202610061343` does not include the legacy voice service. Earlier TypeSafe-enabled TestFlight builds have
different controls and may also send optional student speech context (Section 5.3).
Updating this policy does not change the behavior of an earlier installed build.

---

## 2. What the app handles and where it is kept

| What | Where it is stored | Can the developer see it? |
|---|---|---|
| Board work (handwriting, text, shapes) | On the device (the app's private storage) | No |
| Lesson materials (PPTX, PDF, HTML, images) | On the device · your iCloud Drive | No |
| Timetable, subjects, units, lessons | On the device | No |
| App settings (board color, pens, fonts) | On the device | No |
| Subscription record (Chalkieboard Pro) | Apple's servers (App Store) | No (handled by Apple) |
| The app's Voice Commands audio | Turned into text on the device and not stored | No |
| Voice Commands transcribed text and selected screen context | On the device with Decisions off; sent to OpenAI with new consent and Decisions on (Section 5.2). Earlier builds: Section 5.3 | No |
| System Siri requests | Handled by Apple under your Siri settings and Apple's policies; the app receives the requested action | No (handled by Apple) |
| Your OpenAI voice API key | Separate device Keychain slot; used only with Decisions on. Earlier TypeSafe keys are preserved and unused | No |
| The teacher's voice feature values | On the device (Keychain) | No |
| Classroom scene estimate (scene name, time of change) | In device memory — erased when the class ends. 7 days if 'Keep Class Timeline' is on | No |
| Earlier builds' voice decision log | No new entries; retention cleanup and deletion controls remain available (Section 8) | No |

**There are no Chalkieboard accounts.** Chalkieboard has no sign-up and does not ask you
to register names, email addresses, phone numbers, school names or student identities.
Personal information in your content or spoken commands may be processed as described
in Sections 5 and 7.
Your Apple account for iCloud or the App Store, and any sign-in required by a website
you open, are separate from Chalkieboard. Websites handle their own services under their
own policies.

---

## 3. Device permissions

- **Photos** — Used only when you attach a photo you chose yourself to the board surface.
  The app does not browse your whole photo library and does not send photos externally.
- **iCloud Drive** — The route for opening on the iPad the lesson materials you prepared
  on a Mac or Windows PC. The files are in **your own iCloud account** and do not pass
  through the developer's servers.
- **External display (AirPlay, HDMI)** — When a display is connected, the app sends the
  board screen to it. This output sends only the screen image and does not store any data.
- **Microphone and speech recognition** — Used only if you turn on Voice Commands (Pro) in
  Settings. Sound is turned into text **on this iPad** (on-device dictation). It is not
  recorded or stored, and sound is not sent off the device. **Verify teacher voice** is a separate option,
  off by default. Voice enrollment is required only when this verification is enabled.
  Voice feature values (a list of numbers) are stored only in the device's Keychain.
  With verification off, commands are interpreted from speech heard by the microphone without an identity check.
  You can stop listening with the microphone button. To recognize frequently used commands quickly, the app may
  remember on the device a fingerprint of what was said (a hash value that cannot be
  reversed) and the command name.
- **System actions and Siri** — App Intents expose voice on/off, open lesson, next/previous
  page and pen/eraser actions to Siri and Shortcuts. When invoked through Siri, speech
  processing follows your Siri settings and Apple's policies. The app receives the action
  to perform. These system entry points are separate from the app's microphone-based
  Voice Commands and do not use Decisions (Section 5.1).
- **Classroom scene estimation** — During a class with Voice Commands on, the app examines
  classroom sound **only on this iPad** to guess what kind of scene the class is in, such
  as explanation, group activity or presentations. It uses only numbers, such as how many
  voices there are, the volume, and a score for whether it is the teacher's voice. Sound
  is not sent off the device. This guess is used only to carry out voice commands more
  carefully. The scene guess (scene names and probabilities) is not sent off the device.
  With Decisions on, separate classroom facts such as sound-source labels, loudness and segment
  timing may be sent with a command request (Section 5.2). These facts contain no audio
  or transcript text. A separate, default-off choice can also send recent speech
  and per-voice context to OpenAI (Section 5.2); earlier builds are described in Section 5.3.

---

## 4. Ads

While you use the app for free, the only ads are **rewarded ads that you choose to watch
yourself to top up class time**. Watching one ad adds 1 hour of class time. There are no
banner or full-screen ads that the app shows on its own, and no ads appear during class or
on the external display. Ads are provided by Google AdMob.

- Chalkieboard requests **non-personalized ads only**. It does not use the advertising
  identifier (IDFA) and does not ask for iOS App Tracking Transparency (ATT) permission.
- Even so, AdMob processes basic technical information, such as IP address and device
  type, to show ads and prevent fraudulent clicks. Details of this processing: https://policies.google.com/technologies/partner-sites
- Chalkieboard does not show an ad consent form and does not track you. For users in the EEA, the UK and
  Switzerland, Google serves "limited ads", which do not use personal data to personalize ads.
- **If you subscribe to Chalkieboard Pro, class time becomes unlimited, so you do not need to watch ads.**

Chalkieboard does not separately pass user data to AdMob for advertising purposes.

---

## 5. Voice Commands, optional Decisions and system actions

### 5.1. Apple speech and commands on this iPad

The app transcribes microphone audio with Apple's on-device speech APIs and uses rules on
this iPad for supported commands. This does not require saying “Hey Siri” or turning on
Siri. If Only Listen After Wake Word is off, the app's own wake word is not required either.
Voice Commands requires Pro and the microphone/speech permissions in Section 3. Language
support depends on the device, OS and Apple's language assets; downloading an asset may
need internet. If on-device recognition is unavailable, the app does not silently switch
to server speech recognition.

With Decisions off, supported page/tool commands, supported Korean polite expressions, uniquely
matched material names, explicit English/Korean dictation or reveal commands and uniquely
matched visible app-button names are handled on this iPad. This is a defined set of commands;
it does not promise to understand every sentence. Highlighting selected text and more
flexible requests can use Decisions when you choose to enable it.

The separate App Intents actions turn Voice Commands on/off, open a lesson, turn to the
next/previous page or select pen/eraser. They can be invoked through Shortcuts or system
controls. You can also configure Apple's Vocal Shortcuts in iPad accessibility settings
for a spoken phrase without “Hey Siri”; this is a separate system feature you set up.
When you use Siri, Apple processes that request according to your Siri settings and policies.
Chalkieboard receives the requested action, does not record Siri audio and does not use
Decisions for those actions.

### 5.2. Optional OpenAI Decisions

Decisions is off by default. This update does not inherit TypeSafe keys, the legacy voice-service
setting or its consent. Turning Decisions on requires accepting the new disclosure;
transmission also requires a separately entered OpenAI voice API key. Saving a key does not enable Decisions or
send a connection check. An internet connection and available OpenAI API billing are
required; those charges are separate from Chalkieboard Pro.

With Decisions on, command candidates admitted by the app may include:

- **Command transcripts and alternative transcriptions** — Speech after the app's wake
  word, short follow-ups within 8 seconds of a voice action, or speech without the wake word
  that matches a material, tool, button, function, page number or time. Personal names may
  be included. Teacher verification is optional and imperfect; command candidates are
  not guaranteed to contain only a teacher's words.
- **Selected screen context** — Material, tool and button names; current material/page
  and tool; matching page text and marks; observed text source, position and matching spans;
  recent voice actions and visible app controls. Personal information in this text may be
  included. The app does not send the full document, photo or board-screen recording.
- **Classroom sound facts** — App-produced sound-source labels, loudness, segment timing
  and known activity facts, without audio or transcript text.
- **Web context, with a separate choice** — Web Page Voice Control remains off by default.
  With both choices on, the current web title, offered button/input names and kinds,
  permitted operations and matching visible text may be included. This can include names.
  Opening a website does not enable this choice; websites have their own policies.

**Interpret Speech Beyond Command Words** is a separate, off-by-default choice.
With Decisions on and this choice explicitly accepted, speech candidates and partial
transcripts heard during lessons can reach OpenAI even without a known command word
or a recent voice action. This can include ordinary student speech and personal names.
The same API billing and OpenAI retention terms apply. Only enable this with permission
to share everyone's speech. Only Listen After Wake Word still applies. This choice does
not enable recent speech history or web context; those require their own choices.
Turning it off cancels pending requests and discards late replies but cannot recall
data already received by OpenAI. Turning Decisions off also revokes this choice.

Raw audio, voice features and similarity scores are not sent to OpenAI. Extra recent
student speech, per-voice transcript turns and the accumulated classroom picture are
excluded by default, even when older preferences remain stored. They are included only
after a separate, explicit **Use Classroom Speech Context** choice, which can be turned
off independently. It can include at most two recent student/other transcripts from the
past 20 seconds (160 characters each, 320 total), and up to six earlier per-voice turns
from the past 30 seconds (160 characters each, 480 total), with session-only voice labels
and relative timing. A current turn may add its voice label and timing without repeating
its transcript. Earlier activity and floor estimates, their ages, and the current session's
teacher voice label can also be included. This requires available speaker analysis for
per-voice turns. Transcripts may contain names and other personal information. Recent
context stays in memory on the iPad during the lesson and is cleared when the setting
changes or the lesson closes. Turning it off cancels pending local requests and discards
late results, but cannot recall data already received by OpenAI. A student's words or name
can still appear in an ordinary command candidate or selected screen text even without
this choice. This choice does not enable voice decision logging or erase earlier records.

Preparing the local session sends no HTTP request. **Check Connection (Billed Request)**
sends one fixed synthetic command to OpenAI. Turning Decisions off cancels pending local
requests and discards late results; it keeps the key, materials and existing records.
Cancellation cannot retract data already received or guarantee that the request is free.
To stop microphone commands too, turn Voice Commands off.

The recipient is OpenAI through its API. OpenAI receives the request text/context, API
key for authentication and necessary network information. Its [API data guide](https://developers.openai.com/api/docs/guides/your-data)
says API data is not used for training by default. Default abuse-monitoring logs may retain
customer content for up to 30 days, with exceptions. Prompt caching may retain encrypted
key/value tensors for up to 24 hours. Zero Data Retention requires eligibility and approval and is not
assumed for a personal key. Turning Decisions off is not a server-side deletion request.
Account-specific processing and retention controls follow the user's OpenAI agreement.

### 5.3. Previously installed TestFlight builds

Build `202610061343` excludes TypeSafe: there is no key-entry or transmission option,
and a previously saved key is unused for TypeSafe connections. It preserves existing keys
and logs. Older versions with a legacy voice-service toggle use TypeSafe after their own consent. Neither is the
OpenAI Decisions version described in Section 5.2.

Still earlier TypeSafe-enabled TestFlight builds can send the command-candidate, screen,
web and classroom context described above while Voice Commands is on and a key is available.
They do not have the new independent legacy voice-service consent control. Updating this policy does
not disable an installed older build. To prevent its interpretation requests, avoid entering
a key, remove any saved key in that build's settings, or turn off Voice Commands.

Those older builds can also have these separately enabled transcript-context features:

- **Recent student speech context (optional)** — Transcripts of students' speech are transmitted to TypeSafe in the United States.
  If you turn on Student Speech Context, the existing voice-command request can include up to two recent transcripts
  (at most 160 characters each, from the previous 20 seconds). A segment with evidence of another, non-teacher voice
  may also be included and is labelled `other`, since that voice is not necessarily a student. Segments with unknown
  speaker identity are excluded. This setting is off by default. No additional request is made for this context.
  Enabling it does not replace teacher-voice verification or grant permission to run commands.
- **Per-voice speech turns and the classroom picture (lessons with continuous speaker analysis, optional)** — Transcripts
  of the teacher's, students' and other people's speech are transmitted to TypeSafe in the United States. With continuous
  speaker analysis on, the existing voice-command request can include what was heard in the previous 30 seconds split by
  voice (up to six turns, at most 160 characters each and 480 in total), with the number the app gave each voice (v1…)
  and how many seconds ago it ended. TypeSafe judges who said each turn, the current class activity and who holds the
  floor; the app keeps those judgements (the activity name, who is speaking, the teacher's voice number) only in this
  iPad's memory during the lesson and sends them with the next request. No sound or voice features are sent, and they
  are discarded when the lesson screen closes. The judgements are only used to be more careful about taking speech
  without the wake word as a command; commands called with the wake word are never blocked by them. This setting is off
  by default and no additional request is made for these turns.


These older features do not replace teacher verification or grant permission to execute
commands. Raw audio and voice features remain on the device. Their optional transcript
sharing and old logging behavior are not resumed merely by installing the current version.

---

## 6. Payment

Chalkieboard Pro subscriptions are made only through **App Store in-app purchase**. Apple
handles payment information such as card numbers. Neither the app nor the developer
receives that information. You can manage or cancel your subscription in iOS Settings ▸
Apple Account ▸ Subscriptions. Optional Decisions interpretation is charged by OpenAI to
your own API account; Chalkieboard does not sell API credits or take that payment (Section 5.2).

---

## 7. Children's personal information

Chalkieboard is a tool for teachers, not a student account service. A teacher may include
student names, photos or other personal information in lesson materials or board work.
Those files stay on the device and, if chosen, in the teacher's iCloud. The developer
cannot access them.

With Decisions off, the app sends no command transcripts or screen context to OpenAI. With
Decisions on, a student's name or words in a command candidate, material/button name or matching
page text may be sent to OpenAI (Section 5.2), even without the separate classroom speech
choice. That choice may additionally send the recent student and per-voice transcripts
described in Section 5.2. Web context requires its own choice. Raw student audio is not
sent. Earlier builds are described in Section 5.3.

Use Decisions only for information you are authorized to share, following your school and office
of education's rules and applicable requirements for children's data. A teacher's consent
to Decisions does not by itself establish permission to share another person's information.

---

## 8. Retention and deletion

- If you delete the app, the board work, materials and settings on the device are deleted
  with it.
- **OpenAI voice key and old TypeSafe keys** — The OpenAI voice key has a separate Keychain
  slot. Settings ▸ Voice Control can remove that OpenAI key, turn Decisions off and cancel
  pending requests. Turning Decisions off alone keeps it. The update preserves older
  TypeSafe keys without reading, copying, using or deleting them; this new control does
  not delete those older keys. A saved key alone is not permission to transmit data.
- **Earlier TypeSafe-enabled builds' voice decision log** — In those earlier builds,
  new entries keep only metadata: IDs, stages and types, model name,
  timing, result codes, counts, and diagnostic numbers or fixed states such as analysis
  intervals and verification settings. They do not retain transcribed words, request or
  response bodies, audio, or voice features. If a teacher's voice is registered, though, each
  command turn's similarity score (a number comparing it with the registered voice) is also
  kept in new entries. Entries made by the previous log format
  may still exist and may contain the original speech and interpretation results; you can
  delete them using Delete Stored Decision Logs in Settings ▸ Voice Control (Beta). The log is kept on this device, with a copy in the `판단기록` (decision log)
  folder inside the `Chalkieboard` folder of your own iCloud Drive. It is not sent to the
  developer. The log is on by default in test builds (TestFlight) and off in the App Store
  version. Once entries are older than 30 days or the log exceeds 50MB, the oldest entries are
  deleted first, copies included. You can turn it off or delete it in Settings ▸ Voice Control
  (Beta); deleting it also removes that device's copies. It is not included in device backups.
  The current release does not create the legacy voice service decision-log entries. Automatic retention and
  deletion remain available even when Decisions is off. Cleanup only removes verified
  records owned by this iPad; unknown files and other devices’ copies are preserved.
  Deletion of verified iCloud copies resumes when the same account is available.
  Cleanup does not upload retained historical logs.
- **Class timeline** (when 'Keep Class Timeline' is on) — Only scene names and the times
  they changed are kept, for 7 days.
- The `Chalkieboard` folder in iCloud Drive holds your files, so it remains. If you want to
  remove it, delete it yourself in the Files app or Finder.
- The developer keeps **no** user data. So there is no need to ask the developer to access,
  correct or delete your data.

---

## 9. Sharing with third parties

Chalkieboard does not sell or rent user data. Google AdMob (Section 4), Apple services
including iCloud, the App Store and System Siri (Sections 3, 5.1 and 6), and websites you
choose to open handle their own services under their own policies.

OpenAI Decisions is an optional recipient only after new consent and enablement
(Section 5.2). TypeSafe applies to the older versions described in Section 5.3.

---

## 10. When this policy changes

If this policy changes, the effective date on this page will be updated. Important changes
will be announced in the app.

---

## 11. Contact

- Email: chalkieboard@207studio.dev
- Developer: 207 Studio

Inquiry emails are used only to reply to you, and are deleted once the reply is complete.
