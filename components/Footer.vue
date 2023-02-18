<script lang="tsx">
import { css } from '@emotion/css';
import { addSpace, Colors, Text, Weight } from '~~/assets/rules/Rules';

export default defineComponent({
    render(){

        const footerBodyStyle = css({
            backgroundColor: Colors.WhitePrimary,
            borderTop: `1px solid ${Colors.BorderBasic}`,
            display: 'flex',
            justifyContent: 'center',
            padding: addSpace(2),
        })

        const footerTextStyle = css({
            color: Colors.GrayPrimary,
            fontSize: Text.Type5,
            fontWeight: Weight.Medium,
        })

        return(
            <footer className={footerBodyStyle}>
                <p className={footerTextStyle}>&copy; 2023- nuxt.ayumusaito.dev by AyumuSaito</p>
            </footer>
        )
    }
})
</script>
