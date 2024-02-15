<template>
    <v-container fluid>
        <FeatureCard v-for="ft in myFeatures" :position="ft.position" :src="ft.src" :title="ft.title">
            <div v-html="ft.content.replaceAll('\n', '<br />')" />
        </FeatureCard>
    </v-container>
</template>

<script setup lang="ts">
import FeatureCard from './FeatureCard.vue';
interface Feature {
    position: "right" | "left"
    src: string
    title: string
    content: string
}
const myFeatures: Feature[] = [
    {
        position: "right",
        src: "/pict/nature.jpg",
        title: "翻訳のディレクション＆スケジューリング",
        content: `
複数の言語に同時に翻訳するプロジェクトや、
多量のファイルを翻訳したいケース、
急ぎのため作業を分担させたいときなど、
複数の翻訳者が同時に稼働する際は、効率よくタスクを割り振らないと
パフォーマンスを最大限に発揮できません。
さらに翻訳者によって、使えるソフトもスキルも様々……

ランベージには、翻訳者とプロジェクトマネージャー（PM）両方の経験を持つスタッフが在籍しており、
依頼者と翻訳者の間に入ることで
複雑な案件でも誰もが働きやすいよう、調整役としてお手伝いいたします。
`
    },
    {
        position: "left",
        src: "/pict/nature.jpg",
        title: "翻訳＋αのサービス",
        content: `
翻訳をした訳文は、テキストそのままでは使えないこともあります。

PPTやWord、Excelなどのオフィスファイルに反映したり、
IllustratorやAutoCADなどの専用ソフトに取り込んだり、
動画の字幕にしたり……
はたまた外国語の音声として必要な場合もあるでしょう。

そういった翻訳の「後」に必要な作業も幅広く対応可能です。
`
    },
    {
        position: "right",
        src: "/pict/nature.jpg",
        title: "翻訳用ツール開発",
        content: `
ランベージは「ひつじの翻訳室」と共同で、
翻訳者用便利ツール「TraToys」や、
小規模翻訳会社向け案件管理ツール「ひつじの経理部」などを開発しています。

ほかにもVBAやPythonなどを活用し、
案件ごとのOfficeファイル前処理・後処理作業の自動化なども実施しています。
`
    },
    {
        position: "left",
        src: "/pict/nature.jpg",
        title: "持続可能な翻訳を目指して",
        content: `
機械翻訳やAI翻訳がますます便利になっていく現代。

ランベージはこうした波を「脅威」ではなく、
新しい作業スタイルを確立する「チャンス」だととらえています。

しかしそれは、ある程度自分の翻訳を持っているベテランならではのワザ。
新規参入障壁が高くなっている面も否めません。

ランベージでは、新しい技術を上手く使うための勉強会や、
後進育成のサロンなども積極的に企画し
日本が世界にキャッチアップするための道が
長く続くための貢献をしていきたいと考えています。
`
    },
]

</script>