# Slide Snippets

Reusable slide HTML the `/presentation slides` mode pulls in when a draft
calls for it (an intro, a company overview, the team, a closing CTA). These
aren't part of every deck — they're dropped in on demand. Edit them as your
story and team evolve.

## About me

```html
<div class="slide">
  <h2>About me</h2>
  <ul>
    <li><span class="highlight">{{PRESENTER_NAME}}</span> — {{PRESENTER_ROLE}}</li>
    <li>{{PRESENTER_BACKGROUND}}</li>
    <li>{{PRESENTER_FOCUS}}</li>
  </ul>
</div>
```

## About {{COMPANY}}

```html
<div class="slide">
  <h2>{{COMPANY}}</h2>
  <p>{{COMPANY_TAGLINE}}</p>
  <ul>
    <li>{{COMPANY_POINT_1}}</li>
    <li>{{COMPANY_POINT_2}}</li>
    <li>{{COMPANY_POINT_3}}</li>
  </ul>
</div>
```

## The team

```html
<div class="slide">
  <h2>The team</h2>
  <div class="columns">
    <div>
      <ul>
        {{TEAM_COLUMN_1}}
      </ul>
    </div>
    <div>
      <ul>
        {{TEAM_COLUMN_2}}
      </ul>
    </div>
  </div>
</div>
```

## Connect / CTA

```html
<div class="slide center">
  <p class="big">Let's talk</p>
  <p class="subtitle">{{CONTACT_LINE}}</p>
</div>
```
