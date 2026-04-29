# streaming-tools

OBS-ready streaming widgets.

## Clock widget

Open `widgets/clock/index.html` as an OBS browser source. It is a transparent-background beige clock plate designed for a browser source around `860 x 545`, but it scales to the source size.

Example URL:

```text
file:///Users/u1/Local/atalie2m/GitHub/streaming-tools/widgets/clock/index.html
```

Useful query parameters:

| Parameter | Default | Description |
| --- | --- | --- |
| `tz` | `Asia/Tokyo` | IANA time zone. Example: `Asia/Tokyo`, `America/Los_Angeles`. |
| `seconds` | `1` | Set `seconds=0` to hide seconds. |
| `panel` |  | Override the card color with a hex value, with or without `#`. |
| `light` |  | Override the highlight color used in the plate gradient. |
| `shadow` |  | Override the lower edge color. |
| `ink` |  | Override text color. |
| `saturday` |  | Override Saturday weekday text color. |
| `sunday` |  | Override Sunday weekday text color. |
| `holiday` |  | Override Japanese public holiday weekday text color. |

Examples:

```text
file:///Users/u1/Local/atalie2m/GitHub/streaming-tools/widgets/clock/index.html?seconds=0
file:///Users/u1/Local/atalie2m/GitHub/streaming-tools/widgets/clock/index.html?panel=f1dfc4&light=fff2db&shadow=d2ad7a
```

The weekday color switches to the holiday color on Japanese public holidays. The widget includes Cabinet Office holiday dates for 2026 and 2027, with a rule-based fallback for other years.
# streaming-tools
