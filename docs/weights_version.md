## Vicuna-7B/13B

| Weights Version | v0 | v1.1 |
| ---- | ---- | ---- |
| Link      | [7B](https://huggingface.co/lmsys/vicuna-7b-delta-v0), [13B](https://huggingface.co/lmsys/vicuna-13b-delta-v0) | [7B](https://huggingface.co/lmsys/vicuna-13b-delta-v1-1), [13B](https://huggingface.co/lmsys/vicuna-13b-delta-v1-1) |
| Separator | `###` | `</s>` |
| FastChat PyPI package compatibility | <= v0.1.19 | >= v0.2.0 |
| FastChat source code compatibility  | before [XXXX]() | after [XXXX]() |

Major updates of Weights v1.1
- Refactor the tokenization and separator. In Vicuna v1.1, the separator has been changed from `###` to the EOS token `</s>`. This change makes it easier to determine the generation stop criteria and enables better compatibility with other libraries.
- Fix the supervised fine-tuning loss computation for better model quality.

### Example prompt (v0)
```
A chat between a human and an assistant.

### Human: Hello!
### Assistant: Hello!
### Human: How are you?
### Assistant: I am good.
```
See the full prompt template [here]().

### Example prompt (v1.1)
```
A chat between a user and an assistant.

USER: Hello!
ASSISTANT: Hello!</s>
USER: How are you?
ASSISTANT: I am good.</s>
```

See the full prompt template [here]().
