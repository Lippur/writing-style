# Pass 2: STE80 rules

Examples for each S-rule in SKILL.md. Read this file before you rewrite a long text, when an S-rule is unclear, or before strict mode. The rules paraphrase ASD-STE100. They are not the official text.

## S1. One idea per sentence

A sentence has one subject and one main statement. A procedure step has one action, unless two actions occur at the same time.

> The configuration file, which is loaded at startup and can be overridden by environment variables, controls the cache size as well as the timeout, and should be kept in version control.
> → The configuration file controls the cache size and the timeout. The application reads this file when it starts. Environment variables can override the values in the file. Keep the file in version control.

## S2. Short sentences

Instructions have 20 words or fewer. Descriptions have 25 words or fewer. Aim for an average of about 15. A number with its unit, a code identifier, a name or a quoted string counts as one word.

In 80% mode, a sentence can go a few words over the limit if a split separates a condition from its result. Never go over in strict mode.

## S3. Condition first

If the reader must know a condition before they act, write the condition first, then a comma, then the command.

> Restart the service if the health check fails after the deploy.
> → If the health check fails after the deploy, restart the service.

## S4. Keep the small words

Keep articles (a, an, the), "that" and the verb. Telegraphic text is short but hard to parse. In 80% mode, fragments are acceptable in tables, headings and short UI labels.

> Run script, check output, fix errors found.
> → Run the script. Examine the output. Correct the errors that you find.

## S5. Lists and connectors

If a sentence holds a sequence, a set of options or more than two conditions, make it a vertical list. Number the items if the order matters. Keep reasoning in prose.

Short sentences need clear joints. Use simple connectors: "but", "because", "thus", "as a result", "then", "after", "before", "if", "when". Do not use "however", "furthermore", "moreover" or "additionally".

## S6. Active voice

Name who does the action. Use the passive only in descriptions where the actor is unknown or does not matter.

> The token is validated by the gateway before the request is forwarded.
> → The gateway validates the token. Then it sends the request to the server.

## S7. Simple tenses

Use the simple present, the simple past, the simple future ("will") and the imperative. Do not use perfect or progressive forms ("has been", "is being", "will have", "is running").

> We have been seeing failures that are being caused by a race condition that has existed since 2.3.
> → In version 2.3 and later versions, a race condition causes failures.

## S8. Verbs, not nouns, and no "-ing" chains

Put the action in the verb. "Make a decision" becomes "decide". "Perform an installation of" becomes "install".

Do not use "-ing" forms as verbs. Use them only as a fixed noun ("logging", "caching", "load balancing").

> By enabling the flag, ensuring the cache is warm, and monitoring latency, you can avoid timeouts.
> → To prevent timeouts, do these steps:
> 1. Set the flag.
> 2. Make sure that the cache is warm.
> 3. Monitor the latency.

## S9. Honest modals

STE uses "can" for possibility and ability, "must" for obligation and "will" for the future. Replace "may", "might", "could", "should", "shall" and "would" with one of these, at the same strength of meaning.

If the source is uncertain, keep the uncertainty. "This might fail" becomes "This can fail" or "Possibly, this fails", not "This fails".

## S10. Plain words with one meaning

Pick the short, common word ("use", not "utilise"). `word-swaps.md` has the list.

Use each word in one meaning and as one part of speech. In strict STE, "check" and "test" are nouns only ("do a check"). In 80% mode, follow this only if the double meaning causes confusion.

Replace a phrasal verb with one exact verb. "Set up" becomes "configure" or "install". "Look into" becomes "examine". "Fill in" becomes "complete" or "write".

## S11. One term for each thing

Name each object, concept or role with one term and keep it. Do not switch between "server", "host", "machine" and "node" for the same thing. Readers think that a new word means a new thing.

Technical names (product names, field names, tool names, domain terms) are allowed. Use the name that the reader knows. Write a long term in full once, then use one short form.

## S12. No noun stacks

Use at most three nouns in a row. Break a longer stack with "of", "for" or a relative clause. Hyphenate pairs that act as one unit.

> the user session token refresh retry limit
> → the retry limit for the refresh of the session token

## S13. Paragraphs

Each paragraph has one topic and six sentences at most. Start with the sentence that gives the topic. Go from general to specific. Say what something is before you say how it works. Say what the reader must do before you say why.

## S14. Procedure apart from description, warnings first

Instructions use the imperative ("Open the file."). Descriptions use statements ("The file contains the keys."). Do not mix the two in one paragraph. Put background in a note before or after the steps.

A warning (risk to people) or a caution (risk to data, money or equipment) comes before the step that it protects. Start with the command, then give the risk.

> Running the migration will drop the users table, so make a backup first.
> → **CAUTION:** Make a backup of the database before you run the migration. The migration deletes the users table.

## S15. Punctuation

Use full stops, commas, colons (before lists) and parentheses for short explanations or abbreviations. Do not use semicolons: write two sentences, or use a list. Do not use dashes (§8).

## What 80% mode relaxes

- Vocabulary: use plain common words without the official STE dictionary. Keep words such as "need" or "important" if a swap sounds strange. Never swap a technical term for a vague one.
- Contractions: allowed in casual text, not in documentation.
- "Check" and "test" as verbs: allowed if the meaning is clear.
- Length limits: a small overrun is acceptable if a split hurts the meaning.

80% mode never relaxes these: one idea per sentence, active voice, simple tenses, no filler, one term for each thing, every fact kept.
