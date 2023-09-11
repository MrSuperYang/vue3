<!-- eslint-disable vue/no-v-html -->
<!--
 *           佛曰:  
 *                   写字楼里写字间，写字间里程序员；  
 *                   程序人员写程序，又拿程序换酒钱。  
 *                   酒醒只在网上坐，酒醉还来网下眠；  
 *                   酒醉酒醒日复日，网上网下年复年。  
 *                   但愿老死电脑间，不愿鞠躬老板前；  
 *                   奔驰宝马贵者趣，公交自行程序员。  
 *                   别人笑我忒疯癫，我笑自己命太贱；  
 *                   不见满街漂亮妹，哪个归得程序员？
 * 
 * @Author: qiuming qiuming@tsign.cn
 * @Date: 2023-05-21 14:45:55
 * @LastEditors: qiuming qiuming@tsign.cn
 * @LastEditTime: 2023-09-11 10:38:05
 * @FilePath: /vue3-vite-ts-pinia-master/src/components/DatavUi/Field/src/FieldList.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
 -->

<template>
  <div class="field-item">
    <div class="field-label">
      <template v-if="tooltip">
        <n-tooltip placement="top" class="screen-tip">
          <template #trigger>
            <label class="field-title has-description" :title="label">
              {{ label }}
            </label>
          </template>
          // eslint-disable-next-line vue/no-v-html
          <span v-html="tooltip"></span>
        </n-tooltip>
      </template>
      <label v-else class="field-title" :title="label">
        {{ label }}
      </label>
    </div>
    <div class="field-container">
      <slot></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  label: string
  tooltip?: string
}>()
</script>

<style lang="scss" scoped>
@import './index.scss';
</style>
