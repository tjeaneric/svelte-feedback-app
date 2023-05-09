<script>
    export let style = 'primary'
    export let type = 'button'
    export let disabled = true
</script>

<button {type} {disabled} class={style}>
    <slot></slot>
</button>

<style>
    button{
        color:#fff;
        border:0;
        border-radius: 8px;
        width: 100px;
        height: 40px;
        cursor: pointer;
    }

    button:hover{
      transform: scale(.98);
      opacity: .9;
    }

    button:disabled{
     background-color: #cccccc;
      color: #333;
      cursor: auto;
    }

    button:disabled:hover{
      transform: scale(1);
      opacity: 1;
    }

    .primary{
        background-color: #202142;
    }

    .secondary{
        background-color: #ff6a95;
    }
</style>