<script lang="tsx">import { css } from '@emotion/css';
import { addSpace } from '~~/assets/rules/Rules';
import HomeListItemVue from './HomeListItem.vue';

export default defineComponent({
    render(){

        const homeListContentBodyStyle = css({
            padding: `${addSpace(3)}px 0`,
            "@media (max-width: 480px)":{
                padding: `0 0 ${addSpace(4)}px`,
            }
        })

        const homeListContentListStyle = css({
            display: 'flex',
            gap: addSpace(2),
            justifyContent: 'space-between',
            listStyleType: 'none',
            "@media (max-width: 480px)":{
                flexDirection: 'column',
            }
        })

        return(
            <section className={homeListContentBodyStyle}>
                <ul className={homeListContentListStyle}>
                    <HomeListItemVue />
                </ul>
            </section>
        )
    }
})
</script>