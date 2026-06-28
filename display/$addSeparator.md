# $addSeparator

`$addSeparator` adds a **separator** component to the message. Separators create visual breaks between other components. They go inside containers.

---

## Syntax

```
$addSeparator[(Divider;Spacing;Container ID)]
```

All parameters are optional.

- `Divider`: set to `true` to show a visible line, `false` for just spacing.
- `Spacing`: the size of the spacing around the separator. Either `small` or `large`.
- `Container ID`: optional ID of the container to put this separator inside.

---

## What happens

1. `$addSeparator` creates a separator.
2. If you provide a container ID, it attaches to that container.
3. The separator adds a visual break between the components above and below it.

---

## Example 1: Small spacing with a divider

```
$addContainer[main]
$addTextDisplay[Top section;main]
$addSeparator[true;small;main]
$addTextDisplay[Bottom section;main]
```

What happens:

1. `$addContainer` creates a container.
2. The first text display appears at the top.
3. `$addSeparator` adds a divider line between them.
4. The second text display appears below the divider.

The separator creates a clear visual break between the two text displays.

---

## Example 2: Large spacing without a divider

```
$addContainer[main]
$addTextDisplay[First block;main]
$addSeparator[false;large;main]
$addTextDisplay[Second block;main]
```

What happens:

1. `$addSeparator` adds extra vertical space with no visible line.
2. The two text displays appear separated by a larger gap.

This is useful when you want spacing without a dividing line.

---

## Common uses

- **Separating different sections** of content in a container
- **Adding spacing** between components for better readability
- **Grouping related content** with dividers

---

## See also

- [$addContainer](../parents/$addContainer.md): to create a container for the separator
