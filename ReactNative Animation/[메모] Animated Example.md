Animated e.g

const rotation = POSITION.y.interpolate({
    inputRange: [-300, 300],
    outputRange: ["-360deg", "360deg"],
  });

 - rotate: 360도 회전 (outputRange가 꼭 숫자이지 않아도 된다.)
 - scale: input/outputRange 값에 따라 크기 확대/축소
 - opacity: input/outputRange 값에 따라 투명도 조절

• useNativeDriver: 애니메이션 작업을 자바스크립트 엔진이 아닌 네이티브 레벨에서 진행하는 옵션으로 레이아웃과 관련 없는 스타일에만 적용할 수 있다. 적용되지 않는 스타일은 useNativeDriver를 false로 해주어야 한다.

