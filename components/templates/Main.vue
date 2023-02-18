<script lang="tsx">
import { css } from '@emotion/css';
import { Display } from '~~/assets/rules/Rules';

export default defineComponent({
    setup(_, { slots }){

        const mainStyle = css ({
            margin: `0 ${'auto'}`,
            width: Display.ContentSize,
        })

        return () => (
            <main className={mainStyle}>
                {slots.default && slots.default()}
            </main>
        )
    }
})
</script>