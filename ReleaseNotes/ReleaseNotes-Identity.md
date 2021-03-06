# Trimble.Identity .NET Release Notes

# 1.0.83

* Fixed: argument checking in case AuthorityUri is not initialized

# 1.0.82

* Fixed: the sign-in using web page is not possible if user uses the Backspace key at least once while typing in his credentials

* The JavaScript errors suppression is removed

# 1.0.81

* AuthenticationContext.Parameters property is initialized to default on the context creation in Windows builds.

# 1.0.80

* Support for Owner Password Flow added

* Support for implicit flow removed

* Custom sign-in UI support with auth code flow is removed. The browser behavior is not emulated any more, but user must interact with real browser.

* Trailing slash is automatically added to authority URL if needed.

* Incompatible API changes in the AuthenticationContext constructor: client app registration details are given in the AuthenticationContext constructor instead of individual method calls.

# 1.0.79

* Package metadata is updated with project url, license url and icon, license acceptance is enforced.

# 1.0.78

* Error response parsing improved for the implicit flow. Workaround for [TDEVOPS-4183](https://ejira.trimble.com/browse/TDEVOPS-4183) implemented.

# 1.0.77

* Web sign out (LogoutAsync() method) is fixed (available only for desktop apps).

# 1.0.76

* More tracing added to interactive web sign-in control.

* Logic for web browser control session counting fixed (both for pop-up and embedded): by default session is kept alive while app is running, to kill the session and clear memory state app must call LogoutAsync()

# 1.0.75

* ThirdPartyNotices.txt added to binary distribution with ADAL.NET license.

# 1.0.74

* License text updated to TRIMBLE CONNECT SDK LICENSE AGREEMENT Version 1.0.

# 1.0.73

* Memory leak fixed for embedded web sign control.

# 1.0.72

* License.txt file added to binary distribution.

# 1.0.70

* Support for embedding web sign-in form into the application frame.

* Fix the back key handling in web sign-in form

* Navigating and DocumentCompleted callbacks added

# 1.0.69

* new code signature (Trimble Solutions)

* Tracing fixed to use Warning level instead of WriteLine.

# 1.0.67

* LogoutAsync() method implemented to clear the web session when using the web browser based sign-in.

# 1.0.66

* The HTML page title is used as a fallback if application does not provide a title.

# 1.0.65

* Use Trimble icon as a default for web sign-in popup window.

# 1.0.63

* Allow customizations for web sign-in popup window: title and icon.

# 1.0.58

* package descriptor changed to add links to documentation and license.

# 1.0.55

* no changes.

# 1.0.54

* new icon for nuget package.

# 1.0.53

* New required parameter introduced to the AcquireToken method that uses web browser popup: platform specific parameters. This is a cross platform replacement for AuthenticationContext.OwnerWindow property.

* iOS web browser pop up implemented

* Android web browser pop up implemented

* Forgot password link is now opened in a separate browser window

* Better error message if sign-in web form cannot be parsed

# 1.0.52

* No changes, rebuilt to mark as stable

# 1.0.51-alpha

* .NET 4.0 target platform is now supported

# 1.0.50-alpha

* Use SourceSwitch instead of TraceSwitch to configure logging on mobile platforms

# 1.0.49-alpha

* code tracing added for mobile platforms (see [Developer Guide](Developer%20Guide%20-%20Identity.md))

# 1.0.48-alpha

* code tracing added for desktop platforms (see [Developer Guide](Developer%20Guide%20-%20Identity.md))

# 1.0.47

* OwnerWindow property exposed to apps

# 1.0.45

* fix: pdb file missed in iOS nuget package

# Release 1.0

This release is ment to be a replacement for the GTeam .NET Client component created for Dimentions 2014 integrations.
From now on the GTeam .NET Client component is deprocated and these SDK components should bused instead for all new development.

- Authentication context component works with GTeam authentication mechanism
- web browser pupup for sign-in
- token cache
