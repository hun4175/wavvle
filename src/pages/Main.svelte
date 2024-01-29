<script lang="ts">
    import {Button, Title} from '@svelteuidev/core'
    import WVLButton from '../components/WVLButton.svelte'
    import WVLInput from '../components/WVLInput.svelte'

  /**
   * Main Component
   * wavve-pc
   * 오후 7:37
   * @description
   */
  interface Props {}

  export const props$: Props = {}

  $: ({} = props$)
</script>

<Title>Main</Title>
<WVLButton />
<WVLInput />