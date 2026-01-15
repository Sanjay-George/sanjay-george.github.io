<script>
    import ArrowIcon from "./icons/ArrowIcon.svelte";
    import SkillTag from "./SkillTag.svelte";

    const about = [
        {
            date: "June 2025",
            title: "Service Unit Lead (AI & Research) at newboxes GmbH",
            description:
                "Led platform architecture and delivery for a fast-growing logistics company. Worked with global teams to streamline operations, reduce manual work, and improve release speed. Helped shape internal practices around testing, CI/CD, and collaboration.",
        },
        {
            date: "January 2023",
            title: "Software Engineer at newboxes GmbH",
            description: "",
            skills: ["Node.js", "SQL", "Azure", "CI/CD", "Vue", "PHP"],
        },
        {
            date: "April 2022",
            title: "Moved to Germany for Postgraduate Studies",
            description:
                "Started pursuing MSc in Applied Computer Science at Hochschule Fulda, focusing on AI, cloud computing, data engineering, and distributed systems, strengthening my technical expertise.",
        },
        {
            date: "March 2021",
            title: "Team Lead at CarTrade Tech",
            description:
                "Guided the migration of key systems to modern architecture with high uptime and performance goals. Supported engineers in delivery planning, code standards, and cross-team coordination for large-scale product updates.",
        },
        // {
        //     date: "March 2021",
        //     title: "Team Lead (Used Cars Team) at CarTrade Tech",
        //     description:
        //         "Launched a new used cars product line, boosting revenue streams. Ensured smooth integration with the platform, maintaining high code quality.",
        // },
        {
            date: "June 2018",
            title: "Software Engineer at CarTrade Tech",
            description:
                "Contributed to the development of high-traffic web platforms and helped improve SEO performance and monetization. Collaborated closely with design and product teams to build stable, user-facing features.",
            skills: [".NET C#", "React", "SQL", "Docker", "Kubernetes"],
        },
    ];
</script>

<section id="about" class="h-fit lg:mb-20">
    <p class="section__text__p1 mb-1">
        <span
            class="text-transparent bg-clip-text bg-gradient-to-r to-slate-500
            from-purple-600 dark:to-slate-300">A glimpse at my</span
        >
    </p>
    <h1
        class="title sm:mb-7 mt-0 text-3xl font-extrabold
        md:text-5xl lg:text-6xl text-slate-500 dark:text-slate-200"
    >
        Career Highlights
    </h1>

    <div class="text-xl sm:border sm:rounded-3xl sm:px-16">
        <div class="my-5 sm:my-10 text-slate-500 dark:text-slate-200">
            Software Engineer with 7+ years of experience designing scalable,
            data-driven platforms across logistics, manufacturing, and
            enterprise domains. I focus on improving architecture, automation,
            and team productivity through modern engineering practices.
            <!-- Skilled in leading cross-functional teams, -->
            <!-- modernizing legacy systems, and applying DevOps and AI-driven -->
            <!-- practices to build reliable, high-performing applications. -->
        </div>
        <div>
            <ol class="relative border-s border-slate-200">
                {#each about as item}
                    <li class="mb-6 ml-10 ms-4">
                        <div
                            class="absolute w-3 h-3 bg-slate-200 rounded-full mt-1.5 -start-1.5
                            border border-white"
                        ></div>
                        <time
                            class="text-xs font-extralight leading-none dark:text-slate-50"
                            >{item.date}</time
                        >
                        <h3
                            class="text-xl font-semibold text-slate-900 dark:text-slate-100"
                        >
                            {item.title}
                        </h3>
                        <p
                            class="mb-1 mt-3 sm:text-xl font-normal text-slate-400
                            hover:text-slate-500 transition-colors ease-in-out duration-300"
                        >
                            {item.description}
                        </p>

                        <div>
                            {#if item.skills}
                                {#each item.skills as skill, i}
                                    <SkillTag
                                        color={i % 2 !== 0 ? "purple" : "slate"}
                                        name={skill}
                                    />
                                {/each}
                            {/if}
                        </div>
                    </li>
                {/each}
            </ol>
        </div>
    </div>

    <ArrowIcon scrollTo="#experience" />
</section>
