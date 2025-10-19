<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CenteredTextOnlyHero from "$lib/components/layout/hero-sections/CenteredTextOnlyHero.svelte";

	// Icons
	import IconDroplets from "~icons/lucide/droplets";
	import IconGauge from "~icons/lucide/gauge";
	import IconZap from "~icons/lucide/zap";
	import IconSliders from "~icons/lucide/sliders-horizontal";
	import IconRadar from "~icons/lucide/radar";
	import IconGrid3x3 from "~icons/lucide/grid-3x3";
</script>

<CenteredTextOnlyHero
	title="Accurate probabilities for high-leverage events"
	subtitle="Institutional-grade prediction markets delivering liquid event futures. Trade election outcomes, sports, and market events with tight spreads and deep liquidity."
	imageSrc="/generated/image-a-modern-interior-space-with-a-group-of-.webp"
/>
<LogoScroller
	label="Trusted by traders worldwide"
	logoUrls={[
		'https://cdn.brandfetch.io/coinbase.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/binance.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/draftkings.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/interactivebrokers.com/w/400/h/400/logo'
	]}
/>

<Summary
	title="Built for traders who demand precision"
	text="Totem Markets transforms how sophisticated traders access event-driven alpha. We've built institutional-grade infrastructure that delivers the liquidity and tight spreads missing from traditional prediction markets. Quantitative traders at prop firms and hedge funds finally have a platform that treats event futures with the same rigor as financial derivatives."
/>

<Testimonials
	testimonials={[
		{
			name: "Wei Chen",
			position: "Head of Quantitative Trading",
			company: "Apex Derivatives",
			quote:
				"Totem's tight spreads saved us 2.3% on execution costs across $18M in event contracts. The liquidity depth lets us enter six-figure positions without slippage, which was impossible on competing platforms.",
			image: "/generated/image-headshot-portrait-of-a-professional-asia.webp"
		},
		{
			name: "Amara Okonkwo",
			position: "Principal Strategist",
			company: "Sentinel Capital",
			quote:
				"We reduced our risk exposure by 40% using Totem's real-time probability feeds for portfolio hedging. The institutional-grade infrastructure processes our API orders in under 12ms, giving us the edge we need.",
			image: "/generated/image-headshot-portrait-of-a-professional-blac.webp"
		},
		{
			name: "Reza Hakimi",
			position: "Managing Partner",
			company: "Quantum Prop Trading",
			quote:
				"Totem cut our research time from days to hours. The market's transparent order book and 24/7 liquidity mean we can execute event-driven strategies the moment alpha appears, capturing returns traditional books miss.",
			image: "/generated/image-headshot-portrait-of-a-professional-midd.webp"
		}
	]}
/>

<Features
	title="Built for professional traders"
	subtitle="Institutional-grade infrastructure designed to deliver the liquidity, execution quality, and market coverage that quantitative traders demand."
	features={[
		{
			title: "Deep liquidity pools",
			description:
				"Execute large positions without slippage through our high-performance matching engine that aggregates liquidity from institutional market makers and retail traders.",
			icon: IconDroplets
		},
		{
			title: "Razor-thin spreads",
			description:
				"Access the tightest bid-ask spreads in prediction markets, reducing transaction costs and maximizing returns on every trade you execute.",
			icon: IconGauge
		},
		{
			title: "Instant settlement",
			description:
				"Move capital efficiently with real-time settlement on all trades, eliminating counterparty risk and enabling rapid position rebalancing.",
			icon: IconZap
		},
		{
			title: "Advanced order types",
			description:
				"Deploy sophisticated trading strategies using limit orders, stop losses, and conditional orders designed for professional risk management.",
			icon: IconSliders
		},
		{
			title: "Market intelligence",
			description:
				"Gain information edge through real-time order flow analytics, historical probability data, and sentiment indicators unavailable in traditional markets.",
			icon: IconRadar
		},
		{
			title: "Cross-market coverage",
			description:
				"Trade elections, sports, crypto, and macro events through a unified interface that simplifies portfolio management across diverse event categories.",
			icon: IconGrid3x3
		}
	]}
/>
<AboutTeaser />
<CallToAction
	title="Start trading where probabilities matter"
	subtitle="Join the platform built for serious traders"
	description="Get access to institutional-grade prediction markets with the liquidity and execution quality you've been waiting for. Early traders are already capturing alpha unavailable anywhere else."
	imageSrc="/generated/image-a-professional-quantitative-trader-celeb.webp"
	callsToAction={[
		{
			href: "/get-started",
			label: "Start trading now",
			variant: "primary"
		},
		{
			href: "/contact",
			label: "Talk to our team",
			variant: "secondary"
		}
	]}
/>
