# Tople Palworld PlusPlus
팰월드 멀티플레이 4인 제한을 풀어보자



<p align="center">
  <img alt="Platform" src="https://img.shields.io/badge/platform-Windows%2010%2F11-blue"/>
  <a href="LICENSE"><img alt="License" src="https://img.shields.io/badge/license-MIT-informational"/></a>
</p>



## 빠른 시작가이드

1. [Releases](../../releases) 에서 zip 을 받아 아무 폴더에나 풉니다.
2. **팰월드를 먼저 실행**해서 메인 메뉴까지 들어갑니다.
3. `ToplePalworldPlusPlus.exe` 를 실행합니다.
4. `[1]` 로 원하는 인원을 정합니다. `[3]` 자동 유지는 켜진 채로 둡니다.
5. 게임에서 월드를 **멀티플레이** 로 호스팅합니다.
6. 친구들에게 초대 코드를 알려주면 설정한 인원까지 들어옵니다.

> **월드를 열기 전에** 인원을 설정하세요. 세션의 자리 개수는 호스팅하는
> 순간 정해집니다. 이미 열어둔 상태라면 나갔다가 다시 호스팅하면 됩니다.

> **호스트만** 실행하면 됩니다. 참가하는 친구들은 필요 없습니다.

---

## CLI 가이드

| 번호 | 기능 |
|---|---|
| `1` | 최대 인원 변경 (2~255) |
| `2` | 지금 한 번만 적용 |
| `3` | 자동 유지 시작/중지 — 게임이 값을 되돌려도 계속 다시 씀 |
| `4` | 오브젝트 다시 검색 — 대상을 못 찾을 때 |
| `5` | 현재 메모리에 들어있는 값 보기 |
| `6` | 오프셋 검증 / 진단 |
| `7` | 트레이로 숨기기 |
| `0` | 종료 |

자동 유지는 0.5초마다 값을 확인하고, 월드가 바뀌면 오브젝트를 다시 검색합니다.
마지막으로 정한 인원은 exe 와 같은 폴더 `config.json` 에 저장됩니다.

---

### 패치되는 값들

| `UPalOptionSubsystem.OptionWorldSettings` | `CoopPlayerMaxNum` | +864 +204
| `UPalOptionSubsystem.OptionWorldSettings` | `ServerPlayerMaxNum` | +864 +208
| `UPalOptionSubsystem.OptionWorldSettingsCache` | 위 두 개 | +1384 +204/208
| `UPalGameWorldSettings.OptionSettings` | 위 두 개 | +40 +204/208
| `APalOptionReplicator.OptionWorldSettings` | 위 두 개 | +40 +204/208
| `APalGameStateInGame` | `MaxPlayerNum` | +940
| `AGameSession` | `MaxPlayers` | +660
