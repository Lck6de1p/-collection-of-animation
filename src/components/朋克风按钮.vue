<template>
  <div class="flex-ct-x punk-button css-demo" data-title="朋克风按钮">
    <button>AVAILABLE NOW</button>
  </div>
</template>

<style lang="scss" scoped>
.punk-button {
  min-height: 300px;
}
button, button::after {
  position: relative;
  width: 380px;
  height: 86px;
  font-size: 36px;
  background: linear-gradient(45deg, transparent 5%, #FF013C 5%);
  border: 0;
  color: #fff;
  letter-spacing: 3px;
  line-height: 88px;
  box-shadow: 6px 0px 0px #00E6F6;
  outline: transparent;
  cursor: pointer;
}
button::after {
  --slice-0: inset(50% 50% 50% 50%);
  --slice-1: inset(80% -6px 0 0);
  --slice-2: inset(50% -6px 30% 0);
  --slice-3: inset(10% -6px 85% 0);
  --slice-4: inset(40% -6px 43% 0);
  --slice-5: inset(80% -6px 5% 0);

  content: 'AVAILABLE NOW';
  display: block;
  position: absolute;
  top: 0; left: 0; bottom: 0;
  background: linear-gradient(45deg, transparent 3%, #00E6F6 3%,
  #00E6F6 5%, #FF013C 5%);
  text-shadow: -3px -3px 0px #F8F005, 3px 3px 0px #00E6F6;
  clip-path: var(--slice-0)
}


@keyframes glitch {
  0% {
    clip-path: var(--slice-1);
    transform: translate(-20px, -10px);
  }
  10% {
    clip-path: var(--slice-3);
    transform: translate(10px, 10px);
  }
  20% {
    clip-path: var(--slice-1);
    transform: translate(-10px, 10px);
  }

  30% {
    clip-path: var(--slice-3);
    transform: translate(-0, 5px);
  }
  40% {
    clip-path: var(--slice-2);
    transform: translate(-5px, 0);
  }
  50% {
    clip-path: var(--slice-3);
    transform: translate(5px, 0);
  }
  60% {
    clip-path: var(--slice-4);
    transform: translate(5px, 10px);
  }
  70% {
    clip-path: var(--slice-2);
    transform: translate(-10px, 10px);
  }
  80% {
    clip-path: var(--slice-5);
    transform: translate(20px, -10px);
  }
  90% {
    clip-path: var(--slice-1);
    transform: translate(-10px, 0);
  }
  100% {
    clip-path: var(--slice-1);
    transform: translate(0);
  }
}

button:hover::after {
  animation: glitch 1s;
  animation-timing-function: steps(2, end);
}
</style>