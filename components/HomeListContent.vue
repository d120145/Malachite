<script lang="tsx">import { css } from '@emotion/css';
import { addSpace } from '~~/assets/rules/Rules';
import HomeListItemVue from './HomeListItem.vue';

export default defineComponent({
    render(){

        const homeListContentBodyStyle = css({
            padding: `${addSpace(5)}px 0`,
        })

        const homeListContentListStyle = css({
            display: 'flex',
            gap: addSpace(2),
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