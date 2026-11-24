# Synvector image sizes and art export reference

- **Date:** 2026-11-18
- **Актуализация:** 2026-11-24, после локальных изменений команды и трейлера.
- **Status:** Reference only. No images selected for replacement.
- **Scope:** All **84 raster images** in `public/media/` and `public/media/pp/`.
- **Sources:** Image file headers, `src/GameLanding.jsx`, `index.html` and the current Tailwind configuration.
- **Next step:** Choose replacements after the art team's response, in the next editing iteration.

## Reading the sizes

**All sizes are width × height.** File sizes below are actual image dimensions
in pixels, not screenshot measurements. On-page sizes come from CSS in the
source code; they have not been measured in a running browser.

- **CSS pixels:** How much space the image occupies in the layout.
- **2× export:** Twice the intended display width and height, for sharper
  rendering on high-density screens. It is a planning target, not a fixed requirement.
- **Master:** An original art file from which smaller web exports can be made.
  Do not enlarge a small file and treat the result as a higher-resolution master.
- **Contain:** Shows the full image inside its box, potentially leaving space around it.
- **Cover:** Fills the box and may crop the edges.
- All responsive values assume the default `16px` root font size. Current
  breakpoints: `sm = 640px`, `md = 768px`, `lg = 1024px`, `xl = 1280px`.
- An alpha channel means a file supports transparency; it does not prove
  that every pixel outside the object is transparent.

## 1. Art delivery request: suggested sizes

These are **suggestions for future exports**, not changes to the current layout
and not an approved replacement list. Preserve the intended object scale,
transparent margins and composition; equal canvas sizes alone do not guarantee
equal visual size on the page.

| Image slot | Suggested master / art delivery | Suggested web export | Notes for art |
| --- | --- | --- | --- |
| Team portraits | Square original, **512 × 512 or larger** | **256 × 256** WebP; 512 × 512 if later reuse is needed | В исходнике отображение 100 × 100 CSS px. Экспорт 256px даёт запас 2.56×. Держать лицо по центру с местом для круглой обрезки; не встраивать круг в мастер. Уже предоставленный PNG Anastasia Gorelina в этой итерации не преобразуется в WebP. |
| About the game background (`image 45.png`) | **3840px wide**, height proportional to the chosen composition; about **3840 × 2622** for the existing ratio | **1920px and 2560px wide** versions; select based on actual display and compression | Full-width `cover` background: edges may be cropped. Keep important detail away from edges and behind-text areas. A separate mobile crop may be needed; it is not currently implemented. |
| About the game character (`image 8.png`) | Transparent original at least **1022 × 1174**, same ratio as current art | Up to **1022 × 1174**, then optimize for the approved layout | Desktop only. Height depends on the text card, so recheck after new copy is applied. Supply the whole character and transparent edges, not a flattened background. |
| Tactical Fleet Command / Fleet Customization ship (`Group 94.png`) | Transparent original at least **1440 × 1202**, preserving current ratio | About **1440 × 1202** | Current image box is at most 720px wide. This is a roughly 2× width target. Тексты обновлены локально; замена иллюстрации не выбрана. |
| Gameplay ship (`image 82.png`) | Transparent original at least **2400 × 1467**, preserving current ratio | About **2400 × 1467** | Current CSS caps image width at 1200px. Preserve room around silhouette, effects and glow. |
| FAQ ship (`image 84.png`) | Transparent original at least **1520 × 1379**, preserving current ratio | About **1520 × 1379** | Current CSS uses a fixed 760px width and may clip the illustration on small screens. A smaller export alone will not fix that layout. |
| Hero wordmark (`Logo.png`) | Vector original if available; otherwise the current **2623 × 243** or larger original | Current dimensions are enough for about 2× the current maximum display width | Preserve the wide wordmark ratio. Do not substitute a square logo in this slot without layout review. |
| Steam button background (`Rectangle 28.png`) | Vector or transparent original retaining the intended shape | If keeping its current ratio: about **640 × 127** for 2× the visible image width | Button box is 320 × 92, but `contain` makes the existing artwork about 320 × 64. Do not request 640 × 184 unless deliberately changing the artwork ratio. |
| Partner logo (`partner-supported.webp`) | Vector original, or raster at least the existing **512 × 228** | Existing 512 × 228 is sufficient at the current display size | Maximum display height is 40 CSS px; preserve transparent padding. |
| Footer symbol (`Synvector_Logo_symbol.webp`) | Vector original, or existing **500 × 428** | Existing file is sufficient; a smaller optimized export is optional | Display box is only 20 × 20 CSS px and uses `contain`. |
| Reddit icon (`IconBrandReddit.png`) | Vector if available; otherwise at least **44 × 39**, same ratio | About 44 × 39 or larger, keeping current shape | Box is 22 × 22; source artwork is not square. Do not stretch it to fill the square. |
| Browser favicon | SVG original plus a real square PNG export | **32 × 32** and **64 × 64** PNG; SVG if supported by the delivery workflow | Current HTML references missing PNG/SVG files. Exporting does not update these paths automatically. |
| Optional local trailer poster | Frame from the approved new trailer, **1920 × 1080** | **1920 × 1080** WebP/JPEG | Only needed if a local video or custom thumbnail is used later. В сохранённом неактивном `<video>` poster указывает на MP4. Активный YouTube iframe не использует локальный poster или внешнюю миниатюру до загрузки. |

### Delivery rules

- Supply transparent PNG masters for cutout ships/characters, or another
  agreed source format with alpha. WebP with alpha can be used for delivery to the browser.
- Use sRGB for web exports. Export without captions, UI labels, card borders
  or background panels that the site should render itself.
- For portraits, use filenames containing the approved person's name;
  do not assign people by the existing numeric filenames.
- Keep the original master separately from optimized web images. A multi-megabyte
  portrait original does not need to be served to display a 100px avatar.
- Request pixel dimensions and aspect ratio, not DPI. DPI does not set the
  displayed size of these browser images.
- Recheck final exports after the new texts and team-card layout are approved.
  Large changes in composition may require layout changes, not just a file swap.

## 2. Currently visible non-portrait images

Paths in this table are relative to `public/media/`.

| File | Actual file dimensions | Where used | Display behavior in current code |
| --- | --- | --- | --- |
| `Logo.png` | 2623 × 243 | `Hero`, first-screen logo | `w-full`, `max-w-[1320px]`, natural height, `object-contain`. Parent is `max-w-7xl` with 24px padding each side: effective maximum width about 1232px. |
| `Rectangle 28.png` | 418 × 83 | `Hero`, Steam button background | Button box 320 × 92 CSS px; `background-size: contain`, centered, no repeat. Actual background artwork fits at about 320 × 63.5px. |
| `image 45.png` | 1220 × 833 | `SocialButtons`, About the game background | Entire section background, full available width; `cover`, centered. Height depends on content/padding; no single fixed display size or crop. |
| `image 8.png` | 511 × 587 | `SocialButtons`, character | Hidden below 1024px. At `lg`, height is 130% of the card; at `xl`, 145%; width follows aspect ratio. The card has `md:min-h-[340px]`; if it stays 340px tall, image heights are about 442px / 493px. Longer copy can increase them. |
| `Group 94.png` | 810 × 676 | `InfoBlocks`, ship beside Tactical Fleet Command / Fleet Customization | `w-full`, `max-w-[720px]`, natural height, `contain`; actual width depends on grid column. At 720px wide, image height is about 601px. |
| `image 82.png` | 1324 × 809 | `GameplayBlock`, central ship | `w-[110%]`, `max-w-[1200px]`, natural height, `contain`, absolutely positioned. At 1200px wide, height is about 733px. Section overflow is hidden. |
| `image 84.png` | 849 × 770 | `FAQ`, ship behind questions | Fixed width 760px, `max-w-none`, natural height about 689px, `contain`. Absolutely positioned; may be clipped by section overflow. |
| `IconBrandReddit.png` | 40 × 35 | `Header`, Reddit link | Box 22 × 22px, `contain`; visible artwork fits at about 22 × 19.3px. Link box is 40 × 40px. |
| `partner-supported.webp` | 512 × 228 | `Footer`, Vaiz partner logo | Heights 24px / 32px from `sm` / 40px from `md`, proportional widths about 54px / 72px / 90px. |
| `Synvector_Logo_symbol.webp` | 500 × 428 | `Footer`, copyright symbol | Box 20 × 20px, `contain`; artwork fits at about 20 × 17.1px. |

All ten files above have an alpha channel. This is file metadata, not a
visual check of the transparency margins or a claim that their backgrounds are empty.

YouTube and Discord icons in `Header` are inline SVG components,
`IconBrandYouTube` and `IconBrandDiscord`: `viewBox="0 0 24 24"`, rendered at
22 × 22px. They have no separate raster file to export. Other declared SVG
helpers are not currently rendered in the page.

## 3. Team portraits: actual files and current assignments

All `Ellipse *.png` portraits below support alpha. В локальном исходнике
фото и инициалы занимают **100 × 100 CSS px**, фотографии используют
`object-cover`, центрирование и круглую обрезку (`rounded-full`).
Итоговые 100px заменили предварительные 83px; файлы не пересохранялись.
Исходные портреты 126–127px не обеспечивают 2× разрешения для области 100px:
нужно запросить оригиналы, а не искусственно увеличивать эти файлы.

Имена соответствуют локально применённому
[утверждённому составу](./team_reconciliation.md).
У Sergei Chirko и Vadym Yaroshenko файлов пока нет: показываются `SC` и `VY`.

| File, relative to `public/media/` | Actual dimensions | Current `About.people` assignment |
| --- | --- | --- |
| `anastasia-gorelina.png` | 127 × 127 | Anastasia Gorelina; PNG color type 6, alpha; байты сохранены |
| `Ellipse 1.png` | 127 × 127 | Gleb Kovalevich |
| `Ellipse 2.png` | 127 × 127 | Anton Zarubin |
| `Ellipse 3.png` | 127 × 127 | Andrey Shmanatov |
| `Ellipse 4.png` | 127 × 127 | Not referenced by current page source |
| `Ellipse 5.png` | 127 × 127 | Vladislav Kiselev |
| `Ellipse 6.png` | 127 × 127 | Maksim Dubrovsky |
| `Ellipse 7.png` | 127 × 127 | Не используется текущей страницей; прежняя карточка Alexander Lyulchenko удалена, файл сохранён |
| `Ellipse 8.png` | 127 × 127 | Hanna Patetenka |
| `Ellipse 9.png` | 126 × 126 | Margarita Chebotareva |
| `Ellipse 10.png` | 127 × 127 | Daniil Yuminov |
| `Ellipse 11.png` | 127 × 127 | Viacheslav Grigorenko |
| `Ellipse 12.png` | 127 × 127 | Не используется текущей страницей; прежняя карточка Ewelina Dobrzyanska удалена, файл сохранён |
| `Ellipse 13.png` | 127 × 127 | Artem Stihin |
| `Ellipse 14.png` | 127 × 127 | Not referenced by current page source |
| `Ellipse 15.png` | 126 × 126 | Maksym Novikov |
| `Ellipse 16.png` | 127 × 127 | Not referenced by current page source |
| `Ellipse 17.png` | 127 × 127 | Не используется текущей страницей; прежняя карточка Egor Kirik удалена, файл сохранён |
| `Ellipse 18.png` | 127 × 127 | Aliaksandr Paretski |
| `Ellipse 19.png` | 127 × 127 | Не используется текущей страницей; прежняя карточка Vitaliy Shemyakin удалена, файл сохранён |
| `Ellipse 20.png` | 127 × 127 | Не используется текущей страницей; прежняя карточка Igor Kirichenko удалена, файл сохранён |
| `Ellipse 21.png` | 127 × 127 | Not referenced by current page source |
| `Ellipse 22.png` | 127 × 127 | Artyom Alshevsky |
| `Ellipse 23.png` | 127 × 127 | Sergey Dolzhenko |
| `Ellipse 24.png` | 127 × 127 | Ivan Kalnaus |
| `Ellipse 28.png` | 126 × 126 | Aleksey Aleshin |
| `Ellipse 29.png` | 127 × 127 | Not referenced by current page source |
| `Ellipse 30.png` | 127 × 127 | Pavel Puzyna |
| `Ellipse 31.png` | 127 × 127 | Ekaterina Shumilova |
| `Ellipse 32.png` | 127 × 127 | Simon Shcherbyna |
| `Ellipse 33.png` | 127 × 127 | Sergii Dykhne |
| `Ellipse 34.png` | 127 × 127 | Vladyslav Synookyi |
| `Ellips 32.png` | 1024 × 1024 | Not referenced; different filename from `Ellipse 32.png`. Do not assume the same person from the number. |

## 4. Other existing images: preload-only, unused settings or unreferenced

“Not referenced” means no use found in current `src/` and `index.html`.
It is not permission to delete the file or proof that no external system uses it.

| File, relative to `public/media/` | Actual dimensions | Alpha channel | Current use |
| --- | --- | --- | --- |
| `Synvector_Logo_horizontal.webp` | 620 × 87 | Yes | `MEDIA.logos.header`; preloaded by `GameLanding`, not rendered by `Header`. No active display size. |
| `Synvector_Logo_wordmark.webp` | 500 × 45 | Yes | `MEDIA.logos.hero`; preloaded, but `Hero` renders `Logo.png`. No active display size. |
| `Synvector_Logo_vertical.webp` | 500 × 170 | Yes | Not referenced. |
| `Synvector_Logo.webp` | 650 × 301 | Yes | Not referenced. |
| `slide1.webp` | 1920 × 1080 | No | `MEDIA.infoBlocks[2].img`; the data array is not rendered. |
| `slide2.webp` | 1280 × 720 | No | `MEDIA.infoBlocks[1].img`; the data array is not rendered. |
| `slide3.webp` | 2048 × 1152 | No | `MEDIA.infoBlocks[0].img`; the data array is not rendered. |
| `slide4.webp` | 1280 × 720 | No | `MEDIA.infoBlocks[3].img`; the data array is not rendered. |
| `slide5.webp` | 3840 × 2160 | No | Not referenced. |
| `image 79.png` | 1310 × 120 | Yes | Not referenced. |
| `keyart.png` | 1280 × 716 | Yes | Not referenced. |

The unused `InfoRow` helper would display images with `object-cover` in a
box of `40vh` height (minimum 280px), or from `sm`, `48vh` (minimum 320px).
It is not currently mounted, so those rules do not determine the displayed
sizes of `slide1–4.webp`.

## 5. Additional images in `public/media/pp/`

All 30 files below are WebP without an alpha channel. They are not referenced
by the current page. No identity mapping is inferred from their filenames,
and they are not automatically selected as replacement team photos.
There is no active on-page display size for them.

| File, relative to `public/media/pp/` | Actual dimensions |
| --- | --- |
| `0.webp` | 960 × 960 |
| `1.webp` | 738 × 778 |
| `2.webp` | 640 × 640 |
| `3.webp` | 500 × 500 |
| `4.webp` | 512 × 512 |
| `5.webp` | 900 × 900 |
| `6.webp` | 930 × 754 |
| `7.webp` | 1395 × 2100 |
| `7_2.webp` | 640 × 640 |
| `8.webp` | 450 × 450 |
| `9.webp` | 961 × 1280 |
| `10.webp` | 1012 × 1280 |
| `11.webp` | 3492 × 5238 |
| `12.webp` | 740 × 1114 |
| `13.webp` | 640 × 640 |
| `14.webp` | 960 × 1280 |
| `15.webp` | 1041 × 879 |
| `16.webp` | 960 × 1280 |
| `17.webp` | 3333 × 5000 |
| `18.webp` | 3024 × 4032 |
| `19.webp` | 1991 × 3024 |
| `20.webp` | 300 × 300 |
| `21.webp` | 2880 × 4000 |
| `22.webp` | 833 × 1108 |
| `23.webp` | 712 × 1280 |
| `24.webp` | 1615 × 2524 |
| `32.webp` | 800 × 800 |
| `33.webp` | 1920 × 2560 |
| `34.webp` | 500 × 500 |
| `35.webp` | 800 × 800 |

## 6. Referenced images that are missing

| Requested browser path | Source | Status / sizing note |
| --- | --- | --- |
| `/media/hero-poster.jpg` | `MEDIA.hero.poster`, preloaded by `GameLanding` | File missing. It is not attached to the currently visible `Hero` video. No actual file dimensions. |
| `/media/logo.png` | `MEDIA.logo.poster` | File missing, setting unused. Distinct from existing `Logo.png`; filename case matters on production hosts. |
| `/media/Synvector_Logo_symbol.png` | `index.html`, PNG favicon | File missing. HTML declares `sizes="32x32"`; this is not measured metadata. Existing `.webp` file is a different resource. |
| `/media/favicon.svg` | `index.html`, SVG favicon | File missing. A vector icon has a viewBox / aspect ratio rather than a required raster pixel size. |

`/media/favicon.gif` appears only in a commented HTML example and is also absent;
it is not an active image request.

## 7. Video boundary

`0001-0240.mp4`, `0602.mp4`, `Synvector_02-2.mp4` and `hero.webm` are videos,
not part of the 84-image inventory; their encoded frame dimensions were not
measured for this reference.

- `Hero` displays `0602.mp4` using `object-cover`, full section dimensions
  and `scale-110`; the section is at least one screen tall.
- `Media` создаёт YouTube iframe для `yUzC9Xoque8` при приближении на 300px,
  без автозапуска. Контейнер 16:9, `max-w-5xl` (1024px), горизонтальные
  отступы 24px: максимальная область около 976 × 549 CSS px.
  До создания iframe нет внешней миниатюры; ссылка `Watch on YouTube` постоянная.
- Старый `<video>` с `Synvector_02-2.mp4` сохранён в JSX-комментарии.
  Его `poster` по-прежнему указывает на MP4, а не изображение.
  Файл сохранён, но активный трейлер его не загружает.

## 8. Verification and limitations

- Read PNG IHDR and WebP VP8 / VP8L / VP8X metadata without changing files.
- Count: **54 images in `public/media/` + 30 in `public/media/pp/` = 84**,
  пересчитано 2026-11-24.
- Inventory split: 10 visible non-portrait images + 33 portrait-named PNG
  files (включая Anastasia Gorelina) + 11 other root images + 30 `pp/` files = 84.
- Display rules were checked against the source, not a live browser or
  screenshots. Final crops, clipping, face framing and perceived sharpness
  require visual review after the art team provides files.
- В рамках исходной инвентаризации изображения не менялись. Актуализация
  отражает отдельно разрешённые локальные изменения исходника; байты
  изображений и старого MP4 не изменены. Новые рендеры не выбирались.
- Сборка и браузерная приёмка текущей реализации не подтверждены:
  установленным зависимостям не хватает Windows-модуля Rollup.
