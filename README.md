# Slack Pin Message Steps

This step allows you to pin a message in slack.


---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [SlackPinSteps.zip](SlackPinSteps.zip) - Workflow zip file with the step and example flow
* [slack.png](/slack.png) - GitHub logo

# How it works
This step uses the Slack API to add a pin to a specific message.


# Installation

## Slack Setup
Need to add setup details
-------------------------NOTICE ME-------------------------

## xMatters Setup
1. Download the [SlackPinSteps.zip](SlackPinSteps.zip) file onto your local computer
2. Navigate to the Workflows tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded


## Usage
The **Slack Pin Message** step is now available in your custom steps. So navigate to the appropriate canvas so you can add the step there. If you'd like to experiment with it, the **Pin Message** workflow has a canvas that can be triggered via HTTP call. 

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| Channel | Yes | 0 | 2000 | The human readable channel name, or the channel ID | | No |
| Timestamp | Yes | 0 | 2000 | The timestamp of the message to pin | | No |

Note: the `timestamp` value is an output of the post message Slack step.

### Outputs

| Name | Description |
| ---- | ----------  |
| ok | true or false based on the result of the API call. |
| error | If there is an error in the API call. Otherwise an empty string. |


## Example
This is an example using the slack post message, followed by a slack pin message step. The slack pin message step pins the message from the slack post message step.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

