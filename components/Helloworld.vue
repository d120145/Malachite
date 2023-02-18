<script lang="tsx">
import { css } from '@emotion/css';

export default defineComponent({
    render(){
        const textStyle = css({
            color: 'red',
        })

        return (
            <div>
                <p className={textStyle}>HelloWorld</p>
            </div>
        )
    }
})
</script>