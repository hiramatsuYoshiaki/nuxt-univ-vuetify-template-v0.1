<template lang="pug">
    div.wrape
        div.wizard 
            div.wizard-item
                div.wizard-center-content 
                    div.left-connecter.left-connector-first 
                    div.step-number 1
                    div.right-connecter 
            div.wizard-item
                div.wizard-center-content 
                    div.left-connecter
                    div.step-number 2
                    div.right-connecter
            div.wizard-item
                div.wizard-center-content 
                    div.left-connecter
                    div.step-number 3
                    div.right-connecter.right-connector-last 
</template>

<style lang="scss" scoped>
.wrape {
  /* Content is centered vertically */
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 4px;
}
.wizard {
  display: flex;
  width: 100%;
  height: 100%;
}
.wizard-item {
  // ake all steps have the same width
  flex: 1;
}
.wizard-center-content {
  /* Center the content */
  align-items: center;
  display: flex;
  justify-content: center;
  width: 100%;
  height: 100%;
}
.left-connecter {
  flex: 1;
  height: 1px;

  background-color: rgba(0, 0, 0, 0.3);
  // For the first step, you might need to set it to transparent background:
  // background-color: transparent;
}
.left-connector-first {
  background-color: transparent;
}
.step-number {
  /* Center the content */
  align-items: center;
  display: flex;
  justify-content: center;

  /* Rounded border */
  background-color: rgba(0, 0, 0, 0.3);
  border-radius: 9999px;
  height: 18px;
  width: 18px;

  /* OPTIONAL: Spacing between it and connectors */
  //   margin-left: 4px;
  //   margin-right: 4px;
}
.right-connecter {
  flex: 1;
  height: 1px;

  background-color: rgba(0, 0, 0, 0.3);
  // For the last step, you might need to set it to transparent background:
  // background-color: transparent;
}
.right-connector-last {
  background-color: transparent;
}
</style>
