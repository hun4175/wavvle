<script lang="ts">
    import {Container, InputWrapper, TextInput} from '@svelteuidev/core'
    import {createEventDispatcher} from 'svelte'

  /**
   * WVLInput Component
   * wavve-pc
   * 오후 7:40
   * @description
   */
  interface Props {
    /**
     * @description
     * @default
     */
    maxlength?: number
    /**
     * @description
     * @default
     */
    size?: number
  }

  const dispatch = createEventDispatcher()

  export let props$: Props = {
    maxlength: 1,
    size: 40,
  }

  let value: string = ''

  const onChange = (e: CustomEvent) => {
      if (value.length >= (props$.maxlength?? 0)) {
          console.log(e)
          //dispatch('input', value)
      }
  }
  $: ({size, maxlength} = props$)
</script>

<Container {size}>
    <TextInput {maxlength} bind:value on:keyup={onChange}/>
</Container>
