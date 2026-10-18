- https://youtu.be/2L5ec5o2PuM
## L10: Wrap it with pre trained tokenizer

- Finally, we need to wrap everything in a `PreTrainedTokenizer` class.

- Recall that using `tokenizer.encode` returns `Encoding` with a list of attributes that includes ``ids``, ids `tokens`, `attention_mask` and many more

```python
encoding=tokenizer.encode(text)
print(encoding)
```

- In general, the model requires the `input_ids`, `attention_mask` and other model specific attributes.
-  To get these from the `Encoding` object we need t0
iterate over all the `Encoding` objects corresponding to each sample in a

