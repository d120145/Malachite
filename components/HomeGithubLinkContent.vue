<script lang="tsx">import { css } from '@emotion/css';
import { addSpace, Colors, Hover } from '~~/assets/rules/Rules';
import GithubIcon from '~~/assets/images/image-github_logo.svg';

export default defineComponent ({
    render(){

        const homeGithubLinkContentWrapperStyle = css({
            padding: `${addSpace(3)}px 0`,
            "@media (max-width: 480px)":{
                padding: `0 0 ${addSpace(4)}px`,
            }
        })

        const homeGithubLinkContentBodyStyle = css({
            alignItems: 'center',
            backgroundColor: Colors.WhitePrimary,
            border: `1px solid ${Colors.BorderBasic}`,
            borderRadius: 8,
            display: 'grid',
            gap: addSpace(2),
            justifyItems: 'center',
            padding: addSpace(4),
        })

        const homeGithubLinkContentLinkStyle = css({
            backgroundColor: Colors.WhitePrimary,
            border: `1px solid ${Colors.BorderBasic}`,
            borderRadius: 4,
            color: Colors.GrayPrimary,
            padding: `${addSpace(1)}px ${addSpace(2)}px`,
            textDecoration: 'none',
            transition: Hover.Transition,
            '&:hover':{
                backgroundColor: Colors.GrayTertiary,
            }
        })

        const homeGithubLinkContentImageStyle = css({
            display: 'block',
            height: 32,
            width: 32,
        })

        return (
            <section className={homeGithubLinkContentWrapperStyle}>
                <div className={homeGithubLinkContentBodyStyle}>
                    <img
                    alt=''
                    className={homeGithubLinkContentImageStyle}
                    src={GithubIcon}
                    height={32}
                    width={32}
                    />
                    <a
                    className={homeGithubLinkContentLinkStyle}
                    href='https://github.com/d120145/Malachite'>
                        See GitHub Repository
                    </a>
                </div>
            </section>
        )
    }
})
</script>
