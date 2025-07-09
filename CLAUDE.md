# Claude Code Style Guide
**Use any programming language features to make code as short as possible, while keeping functionality unchanged.**

## Rules
1. Delete all comments.  
2. Remove whitespace, newlines, indentation.  
3. Use any language feature (lambda, ternary, destructuring, chaining, etc.) to minimize code.  
4. Refactor aggressively: use built-ins, inline expressions, avoid loops when map/reduce/filter suffice.  
5. Keep exported names unchanged; rename internal identifiers to short forms.

## Workflow
- Use ES modules (`import/export`), not CommonJS.  
- Prefer destructured imports: `import { x } from 'y'`  
- Run `npm run typecheck` after changes, `npm run build` before commit.  
- Run single tests instead of the whole suite.

## Anti-Patterns
- ❌ Comments  
- ❌ Verbose local names  
- ❌ Multi-line logic  
- ❌ Manual loops over `.map`/`.reduce`

## Example
Before:
```ts
export function double(x: number): number {
  const result = x * 2
  return result
}