# Moodle Azure Logic Apps Connector

An Azure Logic App connector for Moodle.

This connector allows Microsoft [Logic Apps](https://azure.microsoft.com/en-au/services/logic-apps/) and [Power Apps](https://web.powerapps.com/) to interface with several Moodle webservices.<br/>
This allows Moodle functionality to be driven by external sources via Logic Apps.

# Supported Moodle Webservices
The following Moodle webservices are supported by this connector:

* **core\_course\_get\_courses**: Get courses in Moodle instance via webservice functions. Can filter by course ID.
* **core_enrol_get_users_courses**: Get the courses a user is enrolled in.
* **core_user_create_users**: Create new users in Moodle.
* **core_user_delete_users**: Delete Moodle user accounts.
* **core_user_update_users**: Update users in Moodle.
* **mod_forum_add_discussion**: Add a new discussion topic to a Moodle forum.
* **mod_forum_add_discussion_post**: Add a new reply to a Moodle forum discussion topic."

# Moodle Requirements
Before this connector can be used with Moodle the following Moodle plugin needs to be installed:
* https://github.com/catalyst/moodle-webservice_restful

# Crafted by Catalyst IT

This plugin was developed by Catalyst IT Australia:

https://www.catalyst-au.net/

![Catalyst IT](/pix/catalyst-logo.png?raw=true)


# Contributing and Support

Issues, and pull requests using github are welcome and encouraged! 

https://github.com/catalyst/moodle-webservice_restful/issues

If you would like commercial support or would like to sponsor additional improvements
to this plugin please contact us:

https://www.catalyst-au.net/contact-us
