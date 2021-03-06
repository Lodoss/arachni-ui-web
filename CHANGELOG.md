# ChangeLog

## 0.4.4 _(April 12, 2014)_

- External links now open in new windows.

## 0.4.3 _(January 1, 2014)_

- Removed Turbolinks as it breaks Bootstrap modals.
- Updated to use HTML5 `localStorage` instead of cookies to store UI state.
- Navigation menu
    - Removed "Home" item since it was redundant.
    - Updated JS detection of active page when the WebUI is mounted under a subdirectory.
- Profiles
    - Added Regexp validation for the login-check-pattern input.
    - Added Import and Export/Download functionality, supporting:
        - YAML -- Including the CLI AFP files.
        - JSON
    - Delete dialog now warns of the existence of associated Scans.
    - Added support for the `http_queue_size` option.
    - Fixed formatting of cookies as an `RPC::Server::Instance#scan` option.
    - Component selection accordions are now zebra-styled [Issue #57].
- Scans
    - Index
        - Fixed a nil error caused when a Scan's Profile has been deleted.
    - Can now be edited.
    - Can be scheduled, with support for recurring (incremental/differential) Scans.
    - Issues
        - Fixed encoding error when handling request parameters [Issue #39].
        - Redesigned table to group issues by type [Issue #52].
        - Updated severity colors.
    - Reporting
        - Removed Metareport and Text reports as they were unusable via the WebUI.
        - Added proper content-types for all reports.
- Settings
    - Profiles
        - Fixed heading (_Profiles_ => _Plugins_).
    - Added "General" tab.
        - Added Timezone setting.

## 0.4.2.1 _(September 18, 2013)_

- Scan monitoring
    - Keep track of (and restore) the window scroll position between AJAX refreshes.

## 0.4.2 _(August 10, 2013)_

- Fixed bug causing the system to hang after `1:24` hours of scan monitoring,
    caused by improper caching of RPC clients.
- Scan
    - Monitoring
        - Redirect to the Scans list page with an alert if the monitored scan
            was deleted.
- Profiles
    - Added HTTP auth options.

## Version 0.4.1.1 _(July 14, 2013)_

- Login-screen
    - Disabled AJAX refreshing of top-level menu.
- Scan
    - Monitoring
        - Fixed bug causing the error log not to appear when there are errors.

## Version 0.4.1 _(July 06, 2013)_

- Added welcome screen after first sign-in.
- Added support for PostgreSQL along with sample database configuration file (`config/database.yml.pgsql`).
- Added `script/import` to import database and their configurations from older
    packages.
- Switched to <a href="http://github.github.com/github-flavored-markdown/">GitHub-flavored Markdown</a>.
- Profiles
    - Added configuration options for the new platform fingerprinting feature.
- Login page
    - Added a notice for first-time users about the location of the default credentials.
- Scans
    - Index
        - Added resume/pause/abort all buttons.
    - Monitoring
        - Fixed "Share" button to show the modal dialog with the share form.
    - New scan
        - Removed multi-Instance scan warnings and updated Grid behavior as per
            the framework changes.

## Version 0.4 _(April 28, 2013)_

- First version.
