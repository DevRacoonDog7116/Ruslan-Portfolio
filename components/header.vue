<script setup lang="ts">
import { IconLink, IconMapPinFilled } from '@tabler/icons-vue';
</script>

<template>
    <div class="flex items-start sm:items-center justify-between">
        <div class="flex flex-col gap-2 w-2/3">
            <a href="#me">
                <div class="flex flex-row gap-1 items-center group relative">
                    <IconLink
                        class="absolute transform -translate-x-5 transition duration-200 opacity-0 w-4 h-4 group-hover:opacity-100"
                    />
                    <h2 class="text-2xl font-bold hover:cursor-pointer">
                        Ruslan Danyliuk
                    </h2>
                </div>
            </a>
            <div class="my-1">
                <p
                    class="max-w-md text-sm text-neutral-600 dark:text-neutral-400"
                >
                    {{ $t('role') }}
                </p>
                <p
                    class="max-w-md items-center text-xs gap-1.5 inline-flex text-neutral-600 dark:text-neutral-400"
                >
                    <IconMapPinFilled class="w-4 h-4" />
                    Melink, Czeck Republic
                </p>
            </div>
            <div class="flex flex-row gap-2 items-center">
                <UButton
                    icon="i-tabler-brand-github"
                    size="sm"
                    color="primary"
                    variant="soft"
                    square
                    to="https://github.com/Bug-Hunter7116"
                    target="_blank"
                    title="GitHub"
                />
                <UButton
                    icon="i-tabler-brand-linkedin"
                    size="sm"
                    color="primary"
                    variant="soft"
                    square
                    to="https://www.linkedin.com/in/ruslan-danyliuk-163b88346/"
                    target="_blank"
                    title="LinkedIn"
                />
                <UButton
                    icon="i-tabler-phone"
                    size="sm"
                    color="primary"
                    variant="soft"
                    square
                    to="tel:+0427745155738 "
                    arial-label="Phone"
                />
                <UButton
                    icon="i-tabler-mail"
                    size="sm"
                    color="primary"
                    variant="soft"
                    square
                    to="mickaktus@gmail.com"
                    arial-label="Email"
                />
                <UButton
                    icon="i-tabler-file"
                    size="sm"
                    color="primary"
                    variant="soft"
                    square
                    to="/resume"
                    target="_blank"
                    title="Resume"
                />
            </div>
        </div>
        <ClientOnly>
            <ConfettisButton>
                <template v-slot:default="{ onLaunchConfettis }">
                    <img
                        src="/photo.png"
                        alt="Rusaln Danyliuk"
                        class="sm:w-40 sm:h-40 w-24 h-24 rounded-full object-cover hover:cursor-pointer"
                        @click="onLaunchConfettis()"
                    />
                </template>
            </ConfettisButton>
        </ClientOnly>
    </div>
</template>
