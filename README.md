# khal-calendar

Displays the current date and a calendar popup using rofi that integrates with khal calendar.

[![License: GPL v2][license-badge]][license]

## Dependencies

- khal
- rofi
- jq

## Configuration

```ini
[khal-calendar]
command=$SCRIPT_DIR/khal-calendar
interval=60
LABEL=
FONT=mono 12
# Optional: Specify bar position if auto-detection fails
#BAR_POS=top
# Optional: Specify which i3bar to use if you have multiple bars
#BAR_ID=bar-0
# Optional: Custom date formats
#DATEFMT=+%a %d %b %Y
#SHORTFMT=+%d/%m/%Y
# Optional: Custom rofi config file
#ROFI_CONFIG_FILE=/path/to/your/rofi/config
# Optional: Custom rofi width
#ROFI_WIDTH=30%
# Optional: Custom rofi location
#ROFI_LOCATION=northwest
# Optional: Custom rofi calendar options
#ROFI_CALENDAR_OPTIONS="-kb-custom-1 Alt+n \
#                      -kb-custom-2 Alt+p \
#                      -kb-custom-3 Alt+a \
#                      -kb-custom-4 Alt+t"
# Optional: Custom rofi appearance
#TODAY_BG="#005577"
#TODAY_FG="#ffffff"
# Optional: Custom event format
#EVENT_FORMAT="{start-time} {title}"
```

## Features

### Mouse Controls

- **Left Click**: Opens the calendar popup
- **Middle Click**: Shows today's events
- **Right Click**: Shows upcoming events (today and tomorrow)

### Keyboard Shortcuts (when calendar is open)

- **Alt+n**: Next month
- **Alt+p**: Previous month
- **Alt+a**: Add new event
- **Alt+t**: Show today's events
- **Escape**: Close calendar
- **Enter**: Close calendar

### Event Creation

When using Alt+a to add an event, enter the details in the format:

```
YYYY-MM-DD HH:MM Event Name
```

For example: `2024-01-20 14:00 Team Meeting`

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| BAR_POS | bottom | Position of the i3bar (top/bottom) |
| BAR_ID | - | Identifier for specific i3bar when using multiple bars |
| FONT | mono 12 | Font specification for rofi |
| DATEFMT | +%a %d %b %Y | Long date format |
| SHORTFMT | +%d/%m/%Y | Short date format |
| ROFI_CONFIG_FILE | /dev/null | Custom rofi config file |
| ROFI_WIDTH | 30% | Custom rofi width |
| ROFI_LOCATION | northwest | Custom rofi location |
| ROFI_CALENDAR_OPTIONS | -kb-custom-1 Alt+n \ -kb-custom-2 Alt+p \ -kb-custom-3 Alt+a \ -kb-custom-4 Alt+t | Custom rofi calendar options |
| TODAY_BG | #005577 | Custom today background color |
| TODAY_FG | #ffffff | Custom today foreground color |
| EVENT_FORMAT | {start-time} {title} | Custom event format |

## Display

- Default display shows the current date in both long and short formats
- Calendar popup shows the current month with the current day highlighted
- Events are displayed with time and title

## License

[GNU General Public License v2][license]

Copyright (C) 1989, 1991 Free Software Foundation, Inc.

## Contributing

Feel free to submit issues and pull requests on GitHub.

[license]: LICENSE
[license-badge]: https://img.shields.io/badge/License-GPL%20v2-blue.svg
