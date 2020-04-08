# Slack Pin Message Steps

This step allows you to pin a message in Slack.


---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [SlackPinMessageSteps.zip](SlackPinMessageSteps.zip) - Workflow zip file with the step and example flow
* [Slack.png](/Slack.png) - Slack logo

# How it works
This step uses the Slack API to add a pin to a specific message.


# Installation

## Slack Setup
You'll need to setup a Slack app in order to pin messages. Follow [these instructions](https://api.slack.com/authentication/basics) for setting up an app and connecting it to your workspace. Make sure to give it `chat:write` and `pins:write` as User Token Scopes. You should only need to follow the instructions up to the end of the **Installing the app to a workspace** Section.

Once done, take your OAuth User Access Token, found in the **OAuth & Permissions** section of your [app's information](https://api.slack.com/apps), and create a constant in xMatters. Use this constant in the inputs of this step.


## xMatters Setup
1. Download the [SlackPinMessageSteps.zip](SlackPinMessageSteps.zip) file onto your local computer
2. Navigate to the Workflows tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded


## Usage
The **Slack Pin Message** step is now available in your custom steps. So navigate to the appropriate canvas so you can add the step there. If you'd like to experiment with it, the **Slack Pin Message** workflow has a canvas that can be triggered via HTTP call. 

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| Channel | Yes | 0 | 2000 | The human readable channel name, or the channel ID | | No |
| Timestamp | Yes | 0 | 2000 | The timestamp of the message to pin | | No |
| Token | Yes | 0 | 2000 | The OAuth User Access Token from Slack | | No |

Note: the `Timestamp` value is an output of the post message Slack step.

### Outputs

| Name | Description |
| ---- | ----------  |
| ok | true or false based on the result of the API call. |
| error | If there is an error in the API call. Otherwise an empty string. |


## Example
This is an example using the **Slack Post Message Step**, followed by a **Slack Pin Message Step**. The **Slack Pin Message Step** pins the message from the **Slack Post Message Step**.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

