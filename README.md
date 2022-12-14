# ContactsBDayCalendar

This is a simple script to add birthday events of your carddav contacts to your caldav calendar.

## Usage

### Command Line

#### Nextcloud
```
python birthday_calendar.py --contacts_url https://HOST/remote.php/dav/addressbooks/users/USER/contacts/ --calendar_url https://HOST/remote.php/dav/calendars/USER/CALENDAR/ --user USER --password PASSWORD
```
#### Radicale
```
python birthday_calendar.py --contacts_url https://HOST/USER/ADDRESSBOOK-UID/ --calendar_url https://HOST/USER/CALENDAR-UID/ --user USER --password PASSWORD
```

### Docker

You can also run this script in a Docker container

```
docker run ghcr.io/adi146/contacts_bday_calendar:latest --contacts_url https://HOST/remote.php/dav/addressbooks/users/USER/contacts/ --calendar_url https://HOST/remote.php/dav/calendars/USER/CALENDAR/ --user USER --password PASSWORD
```
Or with environment variables
```
docker run --env WEBDAV_CONTACTS_URL=https://HOST/remote.php/dav/addressbooks/users/USER/contacts/ --env WEBDAV_CALENDAR_URL=https://HOST/remote.php/dav/calendars/USER/CALENDAR/ --env WEBDAV_USER=USER --env WEBDAV_PASSWORD=PASSWORD ghcr.io/adi146/contacts_bday_calendar:latest
```
