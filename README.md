# Moodle Azure Logic Apps Connector

An Azure Logic App connector for Moodle.

The connector is provided as an Open API definition file.

This connector allows Microsoft [Logic Apps](https://azure.microsoft.com/en-au/services/logic-apps/) and [Power Apps](https://web.powerapps.com/) to interface with several Moodle webservices.<br/>
This allows Moodle functionality to be driven by external sources via Logic Apps.

More information on Microsoft Logic Apps and how they can help automate your workflows can be found here: https://azure.microsoft.com/en-au/services/logic-apps/

# Supported Moodle Webservices
The following Moodle webservices are supported by this connector:

* **core\_course\_get\_courses**: Get courses in Moodle instance via webservice functions. Can filter by course ID.
* **core_enrol_get_users_courses**: Get the courses a user is enrolled in.
* **core_user_create_users**: Create new users in Moodle.
* **core_user_delete_users**: Delete Moodle user accounts.
* **core_user_update_users**: Update users in Moodle.
* **mod_forum_add_discussion**: Add a new discussion topic to a Moodle forum.
* **mod_forum_add_discussion_post**: Add a new reply to a Moodle forum discussion topic.

More information on Moodle webservices, their usage and configuration can be found on the [Moodle.org](https://moodle.org) website here: https://docs.moodle.org/35/en/Using_web_services

# Moodle Requirements
Before this connector can be used with Moodle the following Moodle plugin needs to be installed and configured:
* https://github.com/catalyst/moodle-webservice_restful

The above Moodle plugin allows Moodle's existing webservices to be communicated with in a RESTful way. This is required as Logic App Connectors require each method of a connected API to be accessed by individual URI endpoints.  This plugin adds this required functionality to Moodle.

## Moodle Access
To use this connector with your Moodle instance your Moodle:
* Must be accessible from the Internet. That is the URL of your Moodle instance must be reachable from a public computer with Internet access.
* Your Moodle must be delivered via HTTPS and have a valid SSL/TLS website certificate.

## Moodle versions
This connector and the above Moodle plugin support the following versions of Moodle:

* 3.1
* 3.2
* 3.3
* 3.4
* 3.5

# Setting up Moodle Webservices

Prior to using this connector with Moodle at least some of the supported Moodle webservices need to be configured and the [Moodle Restful plugin](https://github.com/catalyst/moodle-webservice_restful) needs to be installed.

Setting up Moodle webservices is a multistep porcess and requires a base level of understanding in Moodle operation and administration. It is recommended that an experienced Moodle Administrator be consulted.

Step by step instructions for setting up webservices in Moodle can be found in the Moodle documentation at this link: https://docs.moodle.org/35/en/Using_web_services


# Using this connector in Azure

The Microsoft documentation provides step by step documentation, on how to use set up a custom connector in the Azure Portal using a custom Open API definition file.

Follow this documentation to use this connector to communicate with Moodle.

The documentation can be accessed at: https://docs.microsoft.com/en-gb/connectors/custom-connectors/define-openapi-definition

To set up this connector to use in a workflow you will need:
* To set up the webservices you want to use with this connector in you Moodle instance. (Make sure to only use webservices from the supported list above.)
* The URL of your Moodle instance (must be a public URL).
* The token used to access Moodle webservices, (this is generated as part of the Moodle webservice setup procedure).

# Moodle Outbound Functionality
This connector and the required webservice plugin allow "inbound" connectivity to Moodle. That is they allow Logic Apps to initiate actions in Moodle; such as create users and retrieve data.

Optionally, you can also install the following Moodle plugin to allow Moodle to "trigger" actions in Logic Apps. This allows Moodle to perform "outbound" actions based on events in Moodle.

This Moodle Trigger plugin can be found either from GitHub or the Moodle Plugin Directory using the links below:

* https://github.com/catalyst/moodle-tool_trigger
* https://moodle.org/plugins/tool_trigger

To use this outbound functionality with Azure Logic Apps, you will need to set up the "HTTP Request" Logic App connector. Details on how to setup and use this conenctor can be found at the following link: https://docs.microsoft.com/en-us/azure/connectors/connectors-native-reqres

# Crafted by Catalyst IT

This plugin was developed by Catalyst IT Australia:

https://www.catalyst-au.net/

![Catalyst IT](/pix/catalyst-logo.png?raw=true)


# Contributing and Support

Issues, and pull requests using github are welcome and encouraged! 

https://github.com/catalyst/azure-connector_moodle/issues

If you would like commercial support or would like to sponsor additional improvements
to this plugin please contact us:

https://www.catalyst-au.net/contact-us
