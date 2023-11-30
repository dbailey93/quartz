# Pallet Load Position for End of Line
Once pallet arrives at M2059, the following things occur:
```ad-note
title: Tracking info
1. The tracking code is copied from N80[58] -> N80[59]
2. The tracking code for N80[58] -> zeroes (infoNull)
```

## Pallet Sequence

#### 1. If there is no pallet present on the conveyor and the conveyor is not busy, move pallet

>If [N81[59] = 0] **AND** [M2059.OUT.BUSY = 1]
>Then
>Move [N81[59] from 0 -> 1]

#### 2. If the step sequence of 2059 is at zero, and the conveyor is not busy, then we advance to step 1

>If [selStepsM2059 = 0] **AND** [M2059.OUT.BUSY = 1]
>Move [N81[59] from  0 -> 1]

## Decisions for left and right
---

#### Pre-Step 2.
>The following items move in order through the list if they are true, otherwise it will be pointed out
1. Check if in step 1
2. Check if M2059 is busy
3. If N80[59].Source is equal to N80[60] Source
	1. M2061 A is not busy
		1. **OR** IN[253.1] -> 6700BR1 PE
	2. M2061B is not busy
4. Move [selStepsM2059] to 2

#### Step 2