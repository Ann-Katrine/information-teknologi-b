<template>
    <div>
        <div class="outer-modal">
            <div class="indre-modal">
                <slot>

                </slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'parentModal'
}
</script>

<style>
    .outer-modal{
      z-index: 1;
      display: flex;
      justify-content: center;
      align-content: center;
      position: fixed;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0 ,0 , 0, 50%);        
    }

    .indre-modal{
      background-color: #fff;
      width: 800px;
      min-height: 430px;
      max-height: 100%;
    }
</style>
