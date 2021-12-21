# ⏰ Thai Current Time ![Get Thai Current Time](https://github.com/pluz85/thai-current-time/workflows/Get%20Thai%20Current%20Time/badge.svg) ![units-test](https://github.com/pluz85/thai-current-time/workflows/units-test/badge.svg) ![GitHub release (latest by date)](https://img.shields.io/github/v/release/pluz85/thai-current-time)

This action gets Date and Time in Asia/Bangkok Timezone and output in the Thai language `ภาษาไทย` with Luxon Wrapper. And a modified to display the Thai language in a non-Node environment.

## Outputs

### `thaiTime`

Output time will be in the Thai language and base on Buddist Calendar.

Example : `จ. 11 เม.ย. 63 เวลา 02:06` ✨

## Usage

```yaml
steps:
  - name: Get Thai Current Time
    uses: pk85-sp3ct0r/thai-current-time@1.0
    id: thai-current-time
  - name: Get Time
    env:
      T_TIME: "${{ steps.thai-current-time.outputs.thaiTime }}"
    run: echo $T_TIME
```
