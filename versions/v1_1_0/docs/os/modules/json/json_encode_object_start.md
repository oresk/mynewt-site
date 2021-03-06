## <font color="#F2853F" style="font-size:24pt"> json_encode_object_start </font>

```no-highlight
   int json_encode_object_start(struct json_encoder *encoder)
```

This function starts the encoded JSON object. Usually this means writing out the initial "{" character.

#### Arguments

| Arguments | Description |
|-----------|-------------|
| encoder |  json_encoder to use  |


#### Returned values

0 on success.



#### Example

```c
static int
imgr_list(struct nmgr_jbuf *njb)
{
    struct json_encoder *enc;
    struct json_value array;

    ...

    json_encode_object_start(enc);
    json_encode_object_entry(enc, "images", &array);
    json_encode_object_finish(enc);

    return 0;
}

```
