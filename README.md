# streaming-tools

Japanese README: [README.ja.md](README.ja.md)

OBS-ready streaming widgets.

## Clock Widget

Open `widgets/clock/index.html` as an OBS browser source. It displays a transparent-background beige clock plate. The recommended browser source size is around `860 x 545`, but the widget scales to the source size.

Example URL:

```text
file:///Users/u1/Local/atalie2m/GitHub/streaming-tools/widgets/clock/index.html
```

### URL Parameters

| Parameter | Default | Description |
| --- | --- | --- |
| `tz` | `Asia/Tokyo` | IANA time zone. Example: `Asia/Tokyo`, `America/Los_Angeles`. |
| `seconds` | `1` | Set `seconds=0` to hide the seconds. |
| `panel` |  | Override the plate color with a hex color, with or without `#`. |
| `light` |  | Override the plate highlight color. |
| `shadow` |  | Override the lower plate shadow color. |
| `ink` |  | Override the text color. |
| `saturday` |  | Override the Saturday weekday text color. |
| `sunday` |  | Override the Sunday weekday text color. |
| `holiday` |  | Override the Japanese public holiday weekday text color. |

### Examples

```text
file:///Users/u1/Local/atalie2m/GitHub/streaming-tools/widgets/clock/index.html?seconds=0
file:///Users/u1/Local/atalie2m/GitHub/streaming-tools/widgets/clock/index.html?panel=f1dfc4&light=fff2db&shadow=d2ad7a
```

Weekday text is black on weekdays, blue on Saturdays, and red on Sundays. Japanese public holidays use the holiday color and show the holiday name after the weekday, for example `(WED) 昭和の日`.

The widget includes Cabinet Office holiday and substitute holiday dates for 2026 and 2027. Other years use a rule-based fallback based on Japan's public holiday law.
