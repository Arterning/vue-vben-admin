<script lang="ts" setup>
import { ref } from 'vue';

import { EllipsisText, Page } from '@vben/common-ui';

import { Card } from 'ant-design-vue';

const longText = `Vben Admin 是一个基于 Vue3.0、Vite、 TypeScript 的后台解决方案，目标是为开发中大型项目提供开箱即用的解决方案。包括二次封装组件、utils、hooks、动态菜单、权限校验、多主题配置、按钮级别权限控制等功能。项目会使用前端较新的技术栈，可以作为项目的启动模版，以帮助你快速搭建企业级中后台产品原型。也可以作为一个示例，用于学习 vue3、vite、ts 等主流技术。该项目会持续跟进最新技术，并将其应用在项目中。Vben Admin 是一个基于 Vue3.0、Vite、 TypeScript 的后台解决方案，目标是为开发中大型项目提供开箱即用的解决方案。包括二次封装组件、utils、hooks、动态菜单、权限校验、多主题配置、按钮级别权限控制等功能。项目会使用前端较新的技术栈，可以作为项目的启动模版，以帮助你快速搭建企业级中后台产品原型。也可以作为一个示例，用于学习 vue3、vite、ts 等主流技术。该项目会持续跟进最新技术，并将其应用在项目中。Vben Admin 是一个基于 Vue3.0、Vite、 TypeScript 的后台解决方案，目标是为开发中大型项目提供开箱即用的解决方案。包括二次封装组件、utils、hooks、动态菜单、权限校验、多主题配置、按钮级别权限控制等功能。项目会使用前端较新的技术栈，可以作为项目的启动模版，以帮助你快速搭建企业级中后台产品原型。也可以作为一个示例，用于学习 vue3、vite、ts 等主流技术。该项目会持续跟进最新技术，并将其应用在项目中。Vben Admin 是一个基于 Vue3.0、Vite、 TypeScript 的后台解决方案，目标是为开发中大型项目提供开箱即用的解决方案。包括二次封装组件、utils、hooks、动态菜单、权限校验、多主题配置、按钮级别权限控制等功能。项目会使用前端较新的技术栈，可以作为项目的启动模版，以帮助你快速搭建企业级中后台产品原型。也可以作为一个示例，用于学习 vue3、vite、ts 等主流技术。该项目会持续跟进最新技术，并将其应用在项目中。`;

const text = ref(longText);
</script>

<template>
  <Page
    description="用于多行文本省略，支持点击展开和自定义内容。"
    title="文本省略组件示例"
  >
    <Card class="mb-4" title="基本使用">
      <EllipsisText :max-width="500">{{ text }}</EllipsisText>
    </Card>

    <Card class="mb-4" title="多行省略">
      <EllipsisText :line="2">{{ text }}</EllipsisText>
    </Card>

    <div class="mb-4 flex flex-col lg:flex-row">
      <Card class="mr-3 lg:w-1/2" title="基本使用">
        <EllipsisText>Left</EllipsisText>
      </Card>

      <Card class="lg:w-1/2" title="多行省略">
        <EllipsisText>Right</EllipsisText>
      </Card>
    </div>

    <div class="mb-4 flex flex-col gap-3 md:flex-row">
      <Card class="lg:w-3/5">
        <EllipsisText>A</EllipsisText>
        <p>Content</p>
      </Card>

      <div class="flex flex-row gap-2 lg:w-2/5">
        <Card>
          <EllipsisText>B</EllipsisText>
          <p>Content</p>
        </Card>
        <Card>
          <EllipsisText>C</EllipsisText>
          <p>Content</p>
        </Card>
      </div>
    </div>

    <div
      class="mb-4 flex flex-row items-center justify-between overflow-x-auto pt-4"
    >
      <Card>Menu A</Card>
      <Card>Menu B</Card>
      <Card>Menu C</Card>
    </div>

    <div
      class="3xl:grid-cols-6 mb-4 grid grid-cols-1 gap-8 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5"
    >
      <Card>Item A</Card>
      <Card>Item B</Card>
      <Card>Item C</Card>
      <Card>Item D</Card>
    </div>

    <div
      class="mb-4 grid-cols-2 grid-rows-3 gap-4 lg:grid lg:grid-cols-3 lg:grid-rows-2"
    >
      <div class="rounded-md border p-4 shadow-md">第一行第一列</div>
      <div class="rounded-md border p-4 shadow-md">第一行第二列</div>
      <div class="rounded-md border p-4 shadow-md">第一行第三列</div>
      <div class="rounded-md border p-4 shadow-md">第二行第一列</div>
      <div class="rounded-md border p-4 shadow-md">第二行第二列</div>
      <div class="rounded-md border p-4 shadow-md">第二行第三列</div>
    </div>

    <div className="">
      <div className="container h-full mx-auto xl:px-30 max-w-6xl">
        <div className="grid grid-cols-4 h-full gap-3">
          <div className="border rounded-xl col-span-1 h-full p-4 md:pr-6">
            <div className="flex flex-col items-end">
              <div className="space-y-2 lg:w-[230px]">
                <div>A</div>
                <div>B</div>
                <div>C</div>
              </div>
            </div>
          </div>

          <div
            className="
              border
              rounded-xl
              col-span-3 
              lg:col-span-2 
              border-x-[1px] 
              border-neutral-800"
          ></div>

          <div className="px-6 py-4 hidden lg:block">
            <div className="border rounded-xl p-4">
              <h2 className="text-white text-xl font-semibold">
                Who to follow
              </h2>
              <div className="flex flex-col gap-6 mt-4">
                <div className="flex flex-col">
                  <p className="text-white font-semibold text-sm">Hello</p>
                  <p className="text-neutral-400 text-sm">World</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </Page>
</template>
