# actions-hello

An example GitHub Action

## Inputs

### `salutation`

How should we greet the subject. Default `"Hello"`.

### `subject`

How is being greeted. Default `"World"`.

## Outputs

### `greeting`

The generated greeting

## Example usage

```yaml
steps:
- name: 'Generate Greeting'
  uses: 'bencord0/actions-hello@production'
```

Setting inputs

```yaml
steps:
- name: 'Generate Greeting'
  uses: 'bencord0/actions-hello@production'
  with:
    salutation: 'Hi'
```

Getting outputs

```yaml
steps:
- name: 'Generate Greeting'
  uses: 'bencord0/actions-hello@production'
  id: hello
- run: |
    echo "Greeting: ${{ steps.hello.outputs.greeting }}"
```
