# RAID의 정의와 종류

RAID(Redundant Array of Independent Disks)는 여러 개의 디스크 드라이브를 하나의 논리적 유닛으로 구성하여 데이터의 중복성과 성능을 향상시키는 기술입니다. RAID는 다양한 레벨로 구성되어 있으며, 각 레벨은 데이터 보호와 성능 향상에 대한 다른 접근 방식을 제공합니다.

1. RAID 0 (스트라이핑)
   여러 디스크에 데이터를 나누어 저장합니다.
   높은 성능을 제공하지만, 어느 하나의 디스크가 실패하면 데이터를 복구할 수 없습니다.
2. RAID 1 (미러링)
   두 개의 디스크에 동일한 데이터를 저장하여, 하나의 디스크가 실패해도 다른 하나로부터 데이터를 복구할 수 있습니다.
   데이터 보호에는 유리하지만, 비용이 더 많이 듭니다.
3. RAID 5 (패리티)
   세 개 이상의 디스크를 사용하며, 데이터와 함께 패리티(오류 검출 및 수정 정보)를 저장합니다.
   하나의 디스크가 실패해도 나머지 디스크의 데이터와 패리티를 이용해 데이터를 복구할 수 있습니다.
4. RAID 6 (이중 패리티)
   RAID 5와 유사하지만, 두 개의 패리티를 사용하여 더 높은 데이터 보호를 제공합니다.
   두 개의 디스크가 동시에 실패해도 데이터를 복구할 수 있습니다.
5. RAID 10 (미러링 + 스트라이핑)
   RAID 0과 RAID 1의 조합으로, 미러링된 디스크 세트에서 데이터를 스트라이핑합니다.
   높은 성능과 데이터 보호를 동시에 제공합니다.
   각 RAID 레벨은 사용하는 디스크의 수, 성능, 데이터 보호 수준, 비용 등을 고려하여 선택할 수 있습니다. RAID 구성은 중요한 데이터를 보호하고 시스템의 성능을 향상시키는 데 도움을 줄 수 있습니다.
