<script lang="tsx">
import TsIcon from '~~/assets/images/image-typescript_logo.svg';
import EmotionIcon from '~~/assets/images/image-emotion_logo.svg';
import NetlifyIcon from '~~/assets/images/image-netlify_logo.svg';
import { css } from '@emotion/css';
import { addSpace, Colors, Display, Text, Weight } from '~~/assets/rules/Rules';

export default defineComponent ({
    render(){

        const homeListItemStyle = css({
            backgroundColor: Colors.WhitePrimary,
            border: `1px solid ${Colors.BorderBasic}`,
            borderRadius: 8,
            display: 'grid',
            gap: addSpace(1),
            padding: addSpace(3),
            width: `calc(100%/3 - 16px)`,
            "@media (max-width: 480px)":{
                width: Display.FullSize,
            }
        })

        const homeListItemImageStyle = css({
            display: 'block',
            height: 48,
            width: 48,
        })

        const homeListItemTitleStyle = css({
            color: Colors.BlackPrimary,
            fontSize: Text.Type3,
            fontWeight: Weight.Bold,
        })

        const homeListItemTextStyle = css({
            color: Colors.GrayPrimary,
            fontSize: Text.Type5,
            fontWeight: Weight.Medium,
        })

        const ListItem:{
            image:string,
            title:string,
            description:string,
        }[] = [
            {
                image:TsIcon,
                title: "Only TSX",
                description: ".vue内は<template>と<style>を使用せずに<script>のみで記述しています。"
            },
            {
                image:EmotionIcon,
                title: "@emotion/css",
                description: "@emotion/cssを採用し、tsx内でスタイリングしています。",
            },
            {
                image: NetlifyIcon,
                title: "Auto Deploy",
                description: "MergeしたらNetlifyで自動的にデプロイされるようにしています。"
            },
        ]

        return(
            <>
            {ListItem.map(item => {
                return(
                    <li className={homeListItemStyle}>
                        <img
                        alt=''
                        className={homeListItemImageStyle}
                        src={item.image}
                        height={48}
                        width={48}
                        />
                        <h2 className={homeListItemTitleStyle}>{item.title}</h2>
                        <p className={homeListItemTextStyle}>{item.description}</p>
                    </li>
                )
            })}
            </>
        )
    }
})
</script>
