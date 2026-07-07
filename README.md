# Timezone Shift Planner

Timezone Shift Planner is a personal browser-based planner for converting work schedules into your local timezone, tracking shifts, and marking leave or days off.

Short description: A personal planner that converts work schedules from their original timezone into clear local dates and hours.

## What It Does

Timezone Shift Planner lets you enter work shifts in a source timezone, then view the converted local date and time in a target timezone. It is designed for personal schedule planning, especially when shifts cross midnight or when the source timezone uses daylight saving time.

## Main Features

- Week and month calendar views
- Source-to-local timezone conversion using IANA timezone names
- Overnight shift handling
- Half-hour diagonal boundaries in the week timeline
- Shift-detail popup with source time, local time, type, optional label, edit, and delete
- Custom shift types with saved names and colors
- Leave and day-status tracking for day off, vacation, sick leave, and other statuses
- Import and export of JSON backups
- Fully client-side storage in the browser

## Source And Target Timezones

The source timezone is the timezone where the original schedule was created. The target timezone is the local timezone where you want to view the converted schedule.

Defaults:

- Source timezone: `Europe/Vilnius`
- Target timezone: `Asia/Manila`

The app uses IANA timezone values such as `Europe/Vilnius`, `Asia/Manila`, and `UTC`. Browser timezone handling accounts for daylight saving time when a timezone observes it.

## Adding Shifts

1. Choose one or more days in the current week.
2. Enter the start and end times in the source timezone.
3. Choose a shift type.
4. Optionally add a label.
5. Select **Add to schedule**.

Default shift types are Work, Break, Training, 1-on-1, Meeting, and Other. Use **Manage shift types** to add, edit, or delete custom shift types.

## Marking Leave Or Day Status

Use **Add leave / day status** to apply a status to one date or a range of dates.

Leave types:

- Day Off
- Vacation
- Sick Leave
- Other

Statuses:

- Requested
- Approved
- Declined

Month view shows compact chips for leave information. If a day has both shifts and leave, both are shown.

## LocalStorage

Schedule data is saved automatically in browser `localStorage`. This means the data stays on the same browser and device unless you export and import a backup.

Clearing site data, using another browser, or using another device will not automatically include the same schedule.

## Export And Import

Use the **Backup & transfer** section to export a JSON backup. The backup includes:

- Shifts
- Leave data
- Custom shift types
- Timezone settings
- App settings

Import supports replacing the current data or merging with existing data. Merge avoids duplicate shifts where practical.

## Local Use

Open `index.html` directly in a modern browser. No build step or server is required.

## Vercel Deployment

1. Push this repository to GitHub.
2. In Vercel, create a new project from the repository.
3. Keep the default static deployment settings.
4. Deploy.

The app is a static, client-side site. It does not require a backend, database, login, analytics, or paid service.

## Privacy

No schedule data is sent to a server. Your schedule is saved only in this browser. Export a backup to move it to another device.
