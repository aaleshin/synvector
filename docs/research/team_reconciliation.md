# Synvector team reconciliation — approved roster

- **Author:** Asenok
- **Date:** 2026-11-18
- **Status:** Состав, точные имена и роли, порядок Team и пять удалений утверждены 2026-11-18. Изменения внесены в локальный `src/GameLanding.jsx` 2026-11-24: 24 записи, 22 фото и инициалы `SC` / `VY`. Статическая сверка пройдена; сборка заблокирована отсутствующим Windows-модулем Rollup, браузерная приёмка не выполнена. Публикации и коммитов нет. Исторические заметки ниже — свидетельства сверки, не второй состав команды.
- **Roster authority:** `Synvector_Team.xlsx`, first sheet `Team`, rows 2–25.
- **Additional source:** The user-supplied Team PDF text and images.
- **Website baseline:** `src/GameLanding.jsx`, `About.people` and `About.Person`.

## Final website roster — approved

This is the approved exact public wording: first name, surname and role,
without biographies, nicknames or personal contacts. Names use the checked
LinkedIn spelling where available, or the user's explicit confirmation.
Rows follow the approved Team sheet order. User approval covers these display
names, roles, matches and membership, not the later header experiment or render
replacements.

| # | First name and surname | Website role | Action |
| --- | --- | --- | --- |
| 1 | Aleksey Aleshin | Founder | Keep; update spelling and role |
| 2 | Anastasia Gorelina | Producer | Add; photo supplied as `public/media/anastasia-gorelina.png` |
| 3 | Maksym Novikov | Game designer | Keep; update spelling |
| 4 | Maksim Dubrovsky | Game designer | Keep; update spelling and role |
| 5 | Pavel Puzyna | Lead Narrative Designer | Keep |
| 6 | Ivan Kalnaus | Project Manager | Keep |
| 7 | Andrey Shmanatov | Dev Lead / CTO | Keep; update role |
| 8 | Hanna Patetenka | Developer / UX | Keep existing Anna Potetenko card; update name |
| 9 | Aliaksandr Paretski | Developer | Keep existing Alexander Poretsky card; update name |
| 10 | Margarita Chebotareva | Developer | Keep |
| 11 | Simon Shcherbyna | 3D Lead | Keep |
| 12 | Artem Stihin | 3D Artist | Keep existing Artyom Stikhin card; update name |
| 13 | Artyom Alshevsky | 3D Artist | Keep |
| 14 | Sergei Chirko | 3D Artist | Added locally; initials SC until photo is supplied |
| 15 | Vladislav Kiselev | 3D artist texture | Keep; user-confirmed wording |
| 16 | Daniil Yuminov | Art Director | Keep |
| 17 | Viacheslav Grigorenko | 2D Lead / UI/UX Designer | Keep; update first-name spelling and role; first name before surname |
| 18 | Sergii Dykhne | 2D Concept Artist | Keep; update role |
| 19 | Ekaterina Shumilova | 2D Concept Artist | Keep; same person as Katya / Ignika; update role |
| 20 | Gleb Kovalevich | UI/UX Designer | Keep |
| 21 | Anton Zarubin | Technical Artist | Keep; user-confirmed role |
| 22 | Sergey Dolzhenko | Cinematic 3D Artist / VFX / Rigger | Keep; update role |
| 23 | Vladyslav Synookyi | Sound Designer | Keep |
| 24 | Vadym Yaroshenko | VFX Artist | Added locally; initials VY until photo is supplied |

**Remove five displayed cards:** Alexander Lyulchenko, Egor Kirik,
Vitaliy Shemyakin, Ewelina Dobrzyanska and Igor Kirichenko.
Do not delete their image files as part of this update.

**Photos:** Existing image assignments are recorded below, not independently
verified portraits. Retain the assignments only for the same people; new photos
will be provided separately. Do not borrow another participant's photo for a new card.
No public LinkedIn links are proposed for the cards in this iteration, so
Margarita's differing source URLs do not block roster approval.

## How to read this table

The spreadsheet determines membership and roles, with explicit user-approved
display-role overrides recorded below. LinkedIn is used to check
public full names, not to override a person's role in Synvector.
The website column records the local source code, not a new deployment audit.

All 24 supplied LinkedIn URLs were attempted. Most direct requests returned
HTTP 999 or 429. Where possible, the name was checked against a search result
for that exact profile. Search results can be stale; they are not a substitute
for approval of the spelling people want on the website.

- **Profile:** Name visible in the supplied profile or its exact indexed URL.
- **Alternate:** Name found on another profile URL; the source URL difference needs approval.
- **Pending:** Full name not independently verified. Existing website names
  and URL slugs are clues, not proof of identity.
- **Candidate match:** Proposed link to an existing website card, not a
  confirmed match based on a photograph.

Private email addresses, Telegram handles and dates of birth are intentionally
excluded. Photos have not been downloaded or matched by appearance.

## Team sheet → website

Rows follow spreadsheet order. The role column records the English spreadsheet.
Explicit user-approved website wording is recorded in the action column.

| Excel row / name | Public name found / evidence | Current website card | Role required by Team | Proposed action and checks |
| --- | --- | --- | --- | --- |
| 2 / Aleksey | **Profile:** [Aleksey Aleshin](https://www.linkedin.com/in/greylis-54148a12a/) | Alexey Aleshin — CEO | Founder | Candidate match. Keep person; change role to Founder. Approve Aleksey vs Alexey spelling. |
| 3 / Anastasiya | **Profile index:** [Anastasia Gorelina](https://www.linkedin.com/in/gorelinaai/) | No matching named card | Producer | Approved as Anastasia Gorelina. User supplied photo at `public/media/anastasia-gorelina.png`; keep PNG format for transparency. |
| 4 / Maksim | **Profile index; spelling approved by user:** [Maksym Novikov](https://www.linkedin.com/in/maksym-novikov-92062667/) | Maxim Novikov — Game designer | Game Designer | Keep person; use **Maksym Novikov**, as on LinkedIn. User explicitly approved LinkedIn spelling. |
| 5 / Maksim | **User-confirmed:** Maksim Dubrovsky; [supplied profile](https://www.linkedin.com/in/maksimdubrovsky/) could not be read | Maxim Dubrovsky — Tech Game designer | Technical Game Designer | Keep person; use **Maksim Dubrovsky — Game designer** on the website. User explicitly requested the shorter public role, not Technical Game Designer. Together with Novikov there will be two game designers named Maksim/Maxim/Maksym; they are separate people. |
| 6 / Pavel | **Profile index:** [Pavel Puzyna](https://www.linkedin.com/in/pavel-pusuna-663338207/) | Pavel Puzyna — Lead Narrative designer | Lead Narrative Designer | Candidate match. Keep name; normalize role capitalization. |
| 7 / Ivan | **Profile index:** [Ivan Kalnaus](https://www.linkedin.com/in/ivan-kalnaus-060742227/) | Ivan Kalnaus — Project manager | Project Manager | Candidate match. Keep name; normalize role capitalization. |
| 8 / Andrey | **Profile index:** [Andrey Shmanatov](https://www.linkedin.com/in/andrey-shmanatov-b8a6b6166/) | Andrey Shmanatov — CTO | Dev Lead / CTO | Candidate match. Keep name; update role. |
| 9 / Anya | **Profile index:** [Hanna Patetenka](https://www.linkedin.com/in/hanna-patetenka-277470177/), also indexed at `/in/hanna-patetenka` with North Souls Games | Anna Potetenko — Developer/UX | Developer / UX | Candidate match supported by profile's Synvector work. Approve name correction; retain current photo only after identity confirmation. |
| 10 / Alexander | **Profile index:** [Aliaksandr Paretski](https://www.linkedin.com/in/aliaksandr-paretski-a22661326/), mentions Synvector | Alexander Poretsky — Developer | Developer | Candidate match supported by Synvector work. Approve full name correction; do not add as a second person. |
| 11 / Margarita | **Alternate:** [Margarita Chebotareva](https://www.linkedin.com/in/chebotarevamargarita/), mentions North Souls Games / Synvector | Margarita Chebotareva — Developer | Developer | Candidate match. PDF points to this unhyphenated URL, while Excel uses [chebotareva-margarita](https://www.linkedin.com/in/chebotareva-margarita/). Approve source URL; no name change proposed. |
| 12 / Semyon | **Profile index:** [simon shcherbyna](https://www.linkedin.com/in/simon-shcherbyna/) | Simon Shcherbyna — 3D Lead | 3D Lead | Candidate match. Existing Simon spelling is supported by the supplied public profile; do not automatically transliterate Semyon. |
| 13 / Artem | **Profile index:** [Artem Stihin](https://www.linkedin.com/in/artem-stihin-a90601355/), mentions Synvector | Artyom Stikhin — 3D artist | 3D Artist | Candidate match supported by Synvector work. Approve both first-name and surname spelling changes. |
| 14 / Artem | **Profile index:** [Artyom Alshevsky](https://www.linkedin.com/in/artyom-alshevsky-100379199/) | Artyom Alshevsky — 3D artist | 3D Artist | Candidate match. Keep public name; normalize role capitalization. |
| 15 / Sergey | **Profile index:** [Sergei Chirko](https://www.linkedin.com/in/sergei-chirko-bbb239279/), North Souls Games | No matching named card | 3D Artist | Add after approval; new photo needed. Not the same card as Sergey Dolzhenko. |
| 16 / Vladislav | **User-confirmed:** Vladislav Kiselev; [supplied profile](https://www.linkedin.com/in/vladislav-kiselev-2689382a3/) unavailable | Vladislav Kiselev — 3D artist texture | 3D Texture Artist | Keep person and name; user confirmed website role **3D artist texture**. Do not silently replace it with the spreadsheet's normalized English wording. |
| 17 / Daniil | **Profile index:** [Daniil Yuminov](https://www.linkedin.com/in/daniil-yuminov-91746b1a7/) | Daniil Yuminov — Art Director | Art Director | Candidate match. Keep card; role remains the spreadsheet role, regardless of external job title. |
| 18 / Vyacheslav | **Profile index:** [Grigorenko Viacheslav](https://www.linkedin.com/in/grigorenko-viacheslav-38765a261/) | Vyacheslav Grigorenko — 2D concept artist | 2D Lead / UI/UX Designer | Candidate match. Update role; approve Viacheslav vs Vyacheslav spelling and display order. Do not copy the profile's reversed name order automatically. |
| 19 / Sergey | **Profile index:** [Sergii Dykhne](https://www.linkedin.com/in/sergii-dykhne/) | Sergii Dykhne — 2D artist | 2D Concept Artist | Candidate match. Keep public name; update role. |
| 20 / Katya | **User-confirmed identity:** Katya / Ignika is the existing Ekaterina Shumilova. [Supplied profile](https://www.linkedin.com/in/youcancallmeignika/) remains unavailable; spelling retained from the website, not verified from LinkedIn | Ekaterina Shumilova — 2D artist | 2D Concept Artist | Keep existing person as Ekaterina Shumilova; update role. User confirmed this is the same person and requested full name plus role on each card. |
| 21 / Gleb | **Profile index:** [Gleb Kovalevich](https://www.linkedin.com/in/gleb-kovalevich-52828a26b/) | Gleb Kovalevich — UIUX designer | UI/UX Designer | Candidate match. Keep name; update role formatting. |
| 22 / Anton | **User-confirmed:** Anton Zarubin; [supplied profile](https://www.linkedin.com/in/anzzamaker/) unavailable | Anton Zarubin — TechArt | Technical Artist | Keep person and name; user approved website role **Technical Artist**. |
| 23 / Sergey | **Profile index:** [Sergey Dolzhenko](https://www.linkedin.com/in/sergey-dolzhenko-054a10217/), VFX / motion design and littlefilm website | Sergey Dolzhenko — VFX / Rigger | Cinematic 3D Artist / VFX / Rigger | Candidate match. Keep name; expand role to spreadsheet wording. |
| 24 / Vladislav | **Profile index:** [Vladyslav Synookyi](https://www.linkedin.com/in/vladyslav-synookyi-310b8735a/) | Vladyslav Synookyi — Sound designer | Sound Designer | Candidate match. Keep public name; use spreadsheet role, without adding Lead from the biography. |
| 25 / Vadim | **Profile index:** [Vadym Yaroshenko](https://www.linkedin.com/in/vadym-yaroshenko-76129a226/) | No matching named card | VFX Artist | Add after approval; new photo needed. Do not merge with Egor Kirik just because both work with VFX. |

## Existing website cards without a roster match

Removal below means removal from the displayed team after approval.
It does not mean deleting image files: unused assets may still be needed.

| Current website name | Current role | Current image | Proposed action |
| --- | --- | --- | --- |
| Alexander Lyulchenko | Sound designer | `/media/Ellipse 7.png` | Remove displayed card: no matching person identified in Team. |
| Egor Kirik | VFX/TechArt | `/media/Ellipse 17.png` | Remove displayed card: no matching person identified in Team. |
| Vitaliy Shemyakin | 2D concept artist | `/media/Ellipse 19.png` | Remove displayed card: no matching person identified in Team. |
| Ewelina Dobrzyanska | 2D concept artist | `/media/Ellipse 12.png` | Remove displayed card: no matching person identified in Team. |
| Igor Kirichenko | 2D illustrator artist | `/media/Ellipse 20.png` | Remove displayed card: no matching person identified in Team. |

## Count check

- Current `About.people`: **26 cards**.
- Team sheet: **24 people**.
- Matches to existing cards: **21**, including user-confirmed Katya / Ekaterina; other evidence limits remain noted above.
- New named cards identified: **3** — Anastasia Gorelina, Sergei Chirko, Vadym Yaroshenko.
- User confirmed Katya / Ignika is Ekaterina Shumilova; she is not a new person or a removal.
- Five existing cards proposed for removal.
- Target count: `26 - 5 + 3 = 24`.

## Agreed boundaries for the next iteration

- No biographies on individual cards in this iteration; show photo, first name, surname and role, as explicitly requested by the user. Do not display nicknames or first names alone.
- Increase photo dimensions and both name/role font sizes by about 15%.
  Current source values: photo `72 × 72` CSS pixels, name `12px`, role `10px`.
  Planning values: photo about `83 × 83`, name about `14px`, role about `11.5–12px`.
  Это историческое первоначальное предложение. Итоговое уточнение пользователя:
  **100 × 100 CSS px** для фото/инициалов, имя **14px / 20px**, роль
  **11.5px / 16px**; эти значения внесены в локальный исходник.
  Файлы фотографий не уменьшались. Визуальная проверка ещё не выполнена.
- Add a background and border around each individual card, not only the whole team section.
- Larger text plus a card border reduces available width. Check long names
  and roles before retaining the current six-column desktop layout.
- New photos will be supplied separately. Do not copy LinkedIn photos or
  assign another person's existing photo as a placeholder.
- Website text will describe Synvector as single-player, without co-op or
  multiplayer promises, including the first screen and FAQ.
  Это первоначальная граница обсуждения: итоговая
   [спецификация](../designs/synvector-site-update.md) разрешает только
   три предоставленные замены и удаление пары FAQ. Позже пользователь
   отдельно согласовала удаление `co-op` из Hero без добавления новых
   обещаний; эта точечная правка внесена локально.
- Apply the three supplied text replacements; the old Play Co-op heading
  is intended to become Tactical Fleet Command.
- Trailer target: YouTube video ID `yUzC9Xoque8`, displayed in an embedded YouTube player.
- User explicitly requested retaining the current local `<video>` implementation
  as commented-out JSX, not deleting it and not using a feature flag.
  Keep `public/media/Synvector_02-2.mp4`; switching back would require a code edit.
  The commented player must not remain active or load its video.
  Embedding availability and a usable fallback link still need verification;
  a YouTube URL alone does not guarantee that embedding is enabled.
- Replacement renders depend on art delivery. See [image sizes reference](./image_sizes_reference.md)
  for all current image dimensions and suggested per-slot exports. The user
  will select replacements in the next editing iteration after the team's response.
- Header background is a separate later experiment with a separate approval
  and rollback path. No header redesign is part of roster reconciliation.

## Approval record

On 2026-11-18 the user explicitly confirmed: "да, утверждаем".
The **Final website roster** table, exact names and roles, Team-sheet order
and five removals are approved. Earlier "approve" notes in the research
table are historical evidence and no longer outstanding roster decisions.

This approval does not apply code changes or authorize publication. Anastasia's
photo is supplied at `public/media/anastasia-gorelina.png`; Sergei Chirko and
Vadym Yaroshenko still need their own photos. Render replacements and the later
header experiment remain outside this roster approval.

2026-11-24 пользователь отдельно разрешила локальную реализацию по финальной
спецификации без каких-либо коммитов. Отсутствие фото Sergei Chirko и
Vadym Yaroshenko не блокирует карточки: до поставки файлов используются
инициалы `SC` и `VY`. Результаты и ограничения проверок записаны
в финальной спецификации; изменения не опубликованы.
