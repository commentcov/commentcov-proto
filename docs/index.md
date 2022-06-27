# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [commentcov_plugin.proto](#commentcov_plugin-proto)
    - [Block](#commentcov-plugin-Block)
    - [Comment](#commentcov-plugin-Comment)
    - [CoverageItem](#commentcov-plugin-CoverageItem)
    - [MeasureCoverageIn](#commentcov-plugin-MeasureCoverageIn)
    - [MeasureCoverageOut](#commentcov-plugin-MeasureCoverageOut)
  
    - [CoverageItem.Scope](#commentcov-plugin-CoverageItem-Scope)
  
    - [CommentcovPlugin](#commentcov-plugin-CommentcovPlugin)
  
- [Scalar Value Types](#scalar-value-types)



<a name="commentcov_plugin-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## commentcov_plugin.proto



<a name="commentcov-plugin-Block"></a>

### Block



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| start_line | [uint32](#uint32) |  |  |
| start_column | [uint32](#uint32) |  |  |
| end_line | [uint32](#uint32) |  |  |
| end_column | [uint32](#uint32) |  |  |






<a name="commentcov-plugin-Comment"></a>

### Comment



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| block | [Block](#commentcov-plugin-Block) |  |  |
| comment | [string](#string) |  |  |






<a name="commentcov-plugin-CoverageItem"></a>

### CoverageItem



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| scope | [CoverageItem.Scope](#commentcov-plugin-CoverageItem-Scope) |  |  |
| target_block | [Block](#commentcov-plugin-Block) |  |  |
| file | [string](#string) |  |  |
| identifier | [string](#string) |  |  |
| extension | [string](#string) |  |  |
| header_comments | [Comment](#commentcov-plugin-Comment) | repeated |  |
| inline_comments | [Comment](#commentcov-plugin-Comment) | repeated |  |






<a name="commentcov-plugin-MeasureCoverageIn"></a>

### MeasureCoverageIn



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| files | [string](#string) | repeated |  |






<a name="commentcov-plugin-MeasureCoverageOut"></a>

### MeasureCoverageOut



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| coverage_items | [CoverageItem](#commentcov-plugin-CoverageItem) | repeated |  |





 


<a name="commentcov-plugin-CoverageItem-Scope"></a>

### CoverageItem.Scope


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 |  |
| FILE | 1 |  |
| PUBLIC_MODULE | 2 |  |
| PRIVATE_MODULE | 3 |  |
| PUBLIC_CLASS | 4 |  |
| PRIVATE_CLASS | 5 |  |
| PUBLIC_TYPE | 6 |  |
| PRIVATE_TYPE | 7 |  |
| PUBLIC_FUNCTION | 8 |  |
| PRIVATE_FUNCTION | 9 |  |
| PUBLIC_VARIABLE | 10 |  |
| PRIVATE_VARIABLE | 11 |  |


 

 


<a name="commentcov-plugin-CommentcovPlugin"></a>

### CommentcovPlugin


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| MeasureCoverage | [MeasureCoverageIn](#commentcov-plugin-MeasureCoverageIn) | [MeasureCoverageOut](#commentcov-plugin-MeasureCoverageOut) |  |

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |

