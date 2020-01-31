# Probe Echo docker action

This action echo the message and print the environment and files in current directory.

## Inputs

### `message`

**Required** The message content. Default `"Hello World"`.

## Outputs

### `action_fruit`

Something for output

## Example usage
```
- name: Alpine Probe & Echo
  uses: Kaizhe/alpine-echo@v1.0.0
  with:
    message: 'Hello World!'
  id: alpine_probe_echo
- name: Next Step
  run: |
    echo "What do you get" ${{ steps.alpine_probe_echo.outputs.action_fruit }}
```
