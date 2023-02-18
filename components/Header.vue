<script lang="tsx">
import { css } from '@emotion/css';
import { addSpace, Colors, Text, Weight } from '~~/assets/rules/Rules';
import HeaderLogo from '~~/assets/images/image-fluorite_logo.svg'

export default defineComponent({
    render() {
        const headerBodyStyle = css({
            backgroundColor: Colors.WhitePrimary,
            borderBottom: `1px solid ${Colors.BorderBasic}`,
            display: 'flex',
            justifyContent: 'center',
            padding: addSpace(2),
        })

        const headerContentWrapperStyle = css({
            alignItems: 'center',
            display: 'flex',
            gap: addSpace(1 / 2),
        })

        const headerLogoStyle = css({
            display: 'block',
            height: 32,
            width: 32,
        })

        const headerTextStyle = css({
            color:Colors.BlackPrimary,
            fontSize: Text.Type4,
            fontWeight: Weight.Bold,
        })

        return(
            <header className={headerBodyStyle}>
                <div className={headerContentWrapperStyle}>
                    <img
                    alt=''
                    className={headerLogoStyle}
                    src={HeaderLogo}
                    height={32}
                    width={32}
                    />
                    <p className={headerTextStyle}>.dev</p>
                </div>
            </header>
        )
    }
})
</script>
