<script lang="tsx">
import { css } from '@emotion/css';
import { addSpace, Display } from '~~/assets/rules/Rules';

export default defineComponent({
    setup(_, { slots }){

        const mainStyle = css ({
            margin: `${addSpace(7)}px ${'auto'}`,
            width: Display.ContentSize,
            "@media (max-width: 480px)":{
                margin: `${addSpace(6)}px 0`,
                padding: `0 ${addSpace(3)}px`,
                width: Display.FullSize,
            }
        })

        return () => (
            <main className={mainStyle}>
                {slots.default && slots.default()}
            </main>
        )
    }
})
</script>