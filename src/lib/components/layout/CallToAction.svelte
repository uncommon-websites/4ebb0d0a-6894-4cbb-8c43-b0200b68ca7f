<!--
    @component
    A call-to-action component that attracts attention and encourages user engagement.

    Usage:
    ```html
    <CallToAction
      title="Get started today"
      subtitle="Join now"
      description="Ready to experience the difference? Join our community of satisfied customers and see how our solution can transform your workflow."
      image="https://www.unc.mn/image-placeholder.svg"
      callsToAction={[
        {
          href: "/get-started",
          label: "Get Started",
          variant: "primary"
        },
        {
          href: "/contact",
          label: "Talk to Sales",
          variant: "secondary"
        }
      ]}
    />
    ```

    Props:
    - `title`: The main heading text (string)
    - `subtitle`: Secondary heading text (string)
    - `description`: Detailed information about the offer (string)
    - `callsToAction`: Array of CTA objects with href, label, and optional variant properties (CTA[])
    - `imageSrc`: portrait of the company's customer smiling at the camera.
-->

<script lang="ts">
	// Types
	import type { ComponentProps } from "svelte";

	// Components
	import Button from "../ui/Button.svelte";
	import AnimateText from "../animation/AnimateText.svelte";
	import { cta } from "$lib/navigation";

	// Types
	type CTA = {
		href: string;
		label: string;
		variant?: ComponentProps<typeof Button>["variant"];
	};

	// Props
	const {
		title = "Get started today",
		subtitle = "Join now",
		description = "Ready to experience the difference? Join our community of satisfied customers and see how our solution can transform your workflow. ",
		imageSrc = "https://www.unc.mn/image-placeholder.svg",
		callsToAction = [cta],
		...rest
	}: {
		title?: string;
		subtitle?: string;
		description?: string;
		imageSrc?: string;
		callsToAction?: CTA[];
		[key: string]: any;
	} = $props();
</script>

<div class="" {...rest}>
	<section class="section-px section-py container mx-auto">
		<div
			class="relative grid content-start items-center justify-between gap-(--gap) overflow-hidden rounded-(--radius) p-(--gap) text-balance [--gap:--spacing(8)] [--inner-radius:calc(var(--radius)-var(--gap))] [--radius:var(--radius-xl)] lg:grid-cols-[2fr_1fr]"
			style="background: linear-gradient(135deg, #9B51E0 0%, #FF8A00 50%, #2F80ED 100%);"
		>
			<div class="relative z-10 items-between grid h-full content-between gap-16">
				<h2 class="text-title1 mb-3 flex flex-col text-white">
					<span><AnimateText text={title} /></span>
					<span class="opacity-90"><AnimateText text={subtitle} /></span>
				</h2>
				<div class="flex flex-col items-start justify-start gap-7">
					<p class="text-headline text-white opacity-90">
						{description}
					</p>
					<div class="flex w-full flex-col gap-2 md:flex-row md:flex-wrap">
						{#each callsToAction as cta}
							<Button 
								class={[
									"w-full md:w-auto font-bold transition-all duration-200",
									cta.variant === "primary" ? "bg-[#00F56E] text-gray-950 hover:bg-[#00DD5F]" : "bg-white/10 text-white border border-white/20 hover:bg-white/20"
								]}
								href={cta.href}
								variant={cta.variant || "primary"}
							>
								{cta.label}
							</Button>
						{/each}
					</div>
				</div>
			</div>
			<div class="relative z-10 hidden lg:block">
				<img
					src={imageSrc}
					alt="Successful trader celebrating achievement"
					class="aspect-[4/5] size-full max-h-full w-full rounded-[calc(max(var(--inner-radius),.25rem))] object-cover"
				/>
			</div>
		</div>
	</section>
</div>
