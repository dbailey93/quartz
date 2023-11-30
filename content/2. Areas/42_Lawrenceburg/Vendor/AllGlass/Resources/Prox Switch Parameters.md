# Prox Switch Parameters

### Template
#### Prox Switch Floor Number
Name: 

Item | Parameters
-|-
BF_#: | BF_#
I/O info: | I_#.#
Point I/O Info: | \<A30501_DIN_AI:I:Data[#].#>
Dark (0) or Light (1) | #

```ad-note
I/O info should always be one "one's" place lower than the point I/O location
example:
I_***26.1*** <-> \<A30501_DIN_AI:I:Data***[27].1***>
```

---

#### S38141
Name: Divider 1 Prox. Left

Item | Parameters
-|-
BF_#: | BF_19
I/O info: | I_31.3
Point I/O Info: | \<A30501_DIN_AI:I:Data[32].3>
Dark (0) or Light (1) | 0
#### S38151
Name: Divider 1 Prox. Right

Item | Parameters
-|-
BF_#: | BF_20
I/O info: | I_31.4
Point I/O Info: | \<A30501_DIN_AI:I:Data[32].4>
Dark (0) or Light (1) | 0
