OSINT Template Engine's configurations are stored in json format in a ote.conf configuration file that is located in the installation folder of OTE.

You can easily modify the configuration values and save for the changes to take place. You can also easily reset the configurations to default values that come with OTE, any changes saved or reset will also reset the ote.conf file.

## Engine Configurations

<center><img src="/ssuite/docs/res/engineconfig.png"></center>

* **Timeout:**

Sets the maximum waiting duration in milliseconds for a request to elicit a response from the target server.

`If checked (set to true)`, when maximum timeout is reached and there is no response from target server the request will be aborted and closed.

`If unchecked (set to false)`, the request will remain active until it gets a response from server or until the 30 seconds threshold is reached.

* **User Agent Header**

Sets the `User-Agent` header for the network request. Some template sources do require each request to the server contain a user agent.

`OTE User Agent` - When checked the request will use the OSINT Template Engine's custom agent name (preferred).

`Random User Agent` - When checked the request will use a random user agent from a list of common user agents.

* **Accept Header**

Sets the `Accept` header for the network request to specify the content type that is required. Some template sources uses this header value to determine the content type of the response to send back.

`application/json for json application/xml for xml` - When checked the engine will use the accept header's values `application/json` for json result and `application/xml` for xml. This is the preffered mode.

`all (*/*)` - When checked the engine will use `*/*` value for the accept header indicating that any filtype is accepted.

## General configurations

<center><img src="/ssuite/docs/res/generalconfig.png"></center>

* **Theme**

Configures the general theme of the application, either a light theme or dark theme.

* **Font**

Configures the entire application font type, size and style, simply change the application’s font by using the font dialog.

The changes will take effect after restarting the applicatino.

* **Disable automatic update check**

Disables the automatic check for any available updates for the application which is done when the application is launched (started).

You can still check for updates manually by clicking on the `check for updates` action on the menu bar.