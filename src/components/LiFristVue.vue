<template>
    <div>
        <h2>Hello Li!</h2>
        <ul>
            <li>Age: {{ age }}</li>
            <li>Color: {{ color }}</li>
            <!-- 添加props 步骤5: 将props值显示在浏览器 -->
            <li>{{ treat }}</li>
        </ul>
    </div>
</template>
<script>
export default {
    // 添加props 步骤4: 接受从parent component里的 props 值
    props: ["treat"],
    data: function() {
        return {
          name: "Li",
          age: 6,
          color: "Black"
        };
    }
};
</script>

<style lang="scss">
h2 {
    color: coral;
};
// $color: coral;
// h2 {
//     color: $coral;
// }


</style>


