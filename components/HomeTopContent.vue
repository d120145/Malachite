<script lang="tsx">import { css } from '@emotion/css';
import { addSpace, Colors, Text, Weight } from '~~/assets/rules/Rules';
import emoji from '~~/assets/images/image-victory_hand.svg';

export default defineComponent({
    render(){

        const homeTopContentBodyStyle = css({
            display: 'grid',
            gap: addSpace(1),
            justifyItems: 'center',
            padding: `${addSpace(10)}px 0`,
        })

        const homeTopContentImageStyle = css({
            display: 'block',
            height: 156,
            width: 156,
        })

        const homeTopContentTitleStyle = css({
            color: Colors.BlackPrimary,
            fontSize: 96,
            fontWeight: Weight.Bold,
            lineHeight: '120%',
        })

        const homeTopContentTextStyle = css({
            color: Colors.GrayPrimary,
            fontSize: Text.Type4,
            fontWeight: Weight.Medium,
        })

        return(
            <section className={homeTopContentBodyStyle}>
                <img
                alt=''
                className={homeTopContentImageStyle}
                src={emoji}
                height={156}
                width={156}
                />
                <h1 className={homeTopContentTitleStyle}>Hello! Nuxt</h1>
                <p className={homeTopContentTextStyle}>This is my first Nuxt.js project.</p>
            </section>
        )
    }
})
</script>