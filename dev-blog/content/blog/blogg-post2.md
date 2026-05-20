---
title: Erfaring
description: skole lærdom
date: 2026-05-20
tags: [vue, nuxt, frontend]
author: Student
---

# Dagens intervjue Chorei
```TS 
import { defineContentConfig, defineCollection, z } from "@nuxt/content";

export default defineContentConfig({
  collections: {
    blog: defineCollection({
      type: "page",
      source: "blog/*.md",
      schema: z.object({
        title: z.string(),
        description: z.string(),
        date: z.string(),
        tags: z.array(z.string()).optional(),
        author: z.string().default("Student"),
      }),
    }),
  },
});
```