# Playbook

## What's the playbook?

This was originally a note for the presenter, but I have expanded its capabilities. It now possesses the ability to use TTS and control the interface. The TTS is implemented using the Doubao large model speech synthesis. For control instructions, please refer to the document below.

## Env

Your must be set the api endpoint when you use this feature.

Add the content to `.env` in the root of project.

```env
VITE_DOUBAO_TTS_API=
```

## Control Commands

| Command        | Description                                                                                                |
| -------------- | ---------------------------------------------------------------------------------------------------------- |
| `[next]`       | Like click, jump to the next state. It will jump to the next slide if the state is at the end of the page. |
| `[prev]`       | Jump to the previous state.                                                                                |
| `[go first]`   | Jump to the first page.                                                                                    |
| `[go last]`    | Jump to the last page.                                                                                     |
| `[next slide]` | Jump to the next slide.                                                                                    |

## Control Expressions

| Command           | Description                             | Usage       | Effect              |
| ----------------- | --------------------------------------- | ----------- | ------------------- |
| `[go numbers]`    | Jump to a specific slide                | `[go 1]`    | Jumps to slide 1    |
| `[delay numbers]` | Delay for a specified number of seconds | `[delay 1]` | Delays for 1 second |

## Example

```markdown
So happy today! // It will be spoken by TTS

[delay 2] // It will delay 2s

Today I will be.... // It will be spoken by TTS

```

## Nav Control

| Command                     | Description                                                         |
| --------------------------- | ------------------------------------------------------------------- |
| `Play Current Page Runbook` | It will play the runbook on the current page.                       |
| `Play Global Runbook`       | It will jump to the first page and play the runbook for each slide. |
