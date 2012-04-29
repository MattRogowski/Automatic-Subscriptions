Name: Automatic Subscriptions
Description: Allows you to automatically subscribe to all new threads and replies without having to manually subscribe to all forums and threads.
Website: http://mattrogowski.co.uk/plugins/
Author: MattRogowski
Authorsite: http://mattrogowski.co.uk/plugins/
Version: 1.1
Compatibility: 1.6.x
Files: 2
Templates added: 1
Template changes: 2

Information:
This plugin enables you to get email notifications for all new threads without having to manually subscribe to every forum, and to get email notifications for all new posts without having to manually subscribe to every thread.

To Install:
Upload ./inc/plugins/automaticsubscriptions.php to ./inc/plugins/
Upload ./inc/languages/english/automaticsubscriptions.php to ./inc/languages/english/
Go to ACP > Templates & Style > Templates > **expand template set** > User Control Panel Templates > member_register in the Member Templates [b]and[/b] usercp_options in the User Control Panel Templates > find:
	<tr>
<td colspan="2"><span class="smalltext"><label for="subscriptionmethod">{$lang->subscription_method}</label></span></td>
</tr>
<tr>
<td colspan="2">
	<select name="subscriptionmethod" id="subscriptionmethod">
		<option value="0" {$no_subscribe_selected}>{$lang->no_auto_subscribe}</option>
		<option value="1" {$no_email_subscribe_selected}>{$lang->no_email_subscribe}</option>
		<option value="2" {$instant_email_subscribe_selected}>{$lang->instant_email_subscribe}</option>
	</select>
</td>
</tr>
afterwards, add:
	{$automaticsubscriptions}
Go to ACP > Plugins > Activate

Change Log:
09/05/09 - v0.1 -> Initial 'beta' release.
03/12/11 - v0.1 -> v1.0 -> Added ability to subscribe to threads/posts in subscribed forums only. Made compatible with MyBB 1.6.5. To upgrade, deactivate plugin, reupload ./inc/plugins/automaticsubscriptions.php and ./inc/languages/english/automaticsubscriptions.php, reactivate. Make sure to re-do manual template edit explained above.
XX/XX/XX - v1.0 -> v.1.1 -> Fixed bug that would result in being subscribed to forums/threads you shouldn't have been subscribed to.

Copyright 2011 Matthew Rogowski

 * Licensed under the Apache License, Version 2.0 (the "License");
 * you may not use this file except in compliance with the License.
 * You may obtain a copy of the License at

 ** http://www.apache.org/licenses/LICENSE-2.0

 * Unless required by applicable law or agreed to in writing, software
 * distributed under the License is distributed on an "AS IS" BASIS,
 * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 * See the License for the specific language governing permissions and
 * limitations under the License.