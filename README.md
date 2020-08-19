# UnrealSyslog-docs
Docs for UnrealSyslog Plugin

## Configuration

Once the plugin is installed you can directly configure the list of syslog servers by going to

```Edit/Project Settings/Plugins/Syslog Plugin```:

![UnrealSyslogSettingsSidePanel](Screenshots/UnrealSyslogSide.PNG?raw=true "UnrealSyslogSettingsSidePanel")

The Settings panel will appear (this is an example screenshot with a list of server already specified):

![UnrealSyslogSettings](Screenshots/UnrealSyslogSettings.PNG?raw=true "UnrealSyslogSettings")

Each Syslog server requires an address and a port (you can change them on the fly without restarting the editor).

Facility can be set accordingly to the list available at https://tools.ietf.org/html/rfc5424#section-6.2.1 (the default '1' means 'user-level messages')

Each Unreal Engine log message has an associated category (like LogTemp, LogAudioMixer...). You can specify a list of the categories the specific syslog server will get (WhiteList) or will not get (BlackList).

If your server support UTF8 log messages, you can enable the specific option. Note that some of the server will recognize UTF8 messages using the BOM prefix (https://it.wikipedia.org/wiki/Byte_Order_Mark). In such a case, enable the BOM flag too.


