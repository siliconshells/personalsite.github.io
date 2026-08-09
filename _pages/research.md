---
permalink: /research/
title: "Research"
excerpt: "Research"
author_profile: true
redirect_from: 
  # - /research.html
---

<p style="font-size: 15px; margin: 0 0 8px 0;">
My research looks at whether we can actually supervise AI agents as they get more capable - and, more specifically, where the popular proposals for doing so quietly stop working.
</p>

<div style="display: flex; flex-direction: column; border: 1px solid #8b939bff; border-radius: 8px; padding: 16px; margin: 16px 0; width: 100%; background-color: #fdfdfcff;">

  <div style="flex: 1;">
    <h3 style="margin: 0 0 4px 0;">Credulity, Not Verification: The Limits of Structured Assistance for Tool-Blind Oversight of AI Agents</h3>
    <p style="margin: 0 0 4px 0; font-size: 15px; font-style: italic; color: #4a5158;">
      When a weak overseer cannot independently verify evidence, apparent amplification reflects trust that does not persist under scrutiny by a more skeptical overseer.
    </p>
    <p style="margin: 0 0 14px 0; font-size: 14px; color: #6a7178;">
      Leonard Eshun &nbsp;·&nbsp; Independent Research &nbsp;·&nbsp; 2026
    </p>
  </div>

  <!-- Headline numbers -->
  <div style="display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 16px;">
    <div style="flex: 1 1 150px; border: 1px solid #dfe3e7; border-radius: 6px; padding: 10px 12px; background-color: #f7f9fb;">
      <div style="font-size: 22px; font-weight: bold; color: #0955abff;">0.00</div>
      <div style="font-size: 13px; color: #4a5158;">Detection of a fabricated tool output by an unaided overseer - at <em>every</em> capability tier</div>
    </div>
    <div style="flex: 1 1 150px; border: 1px solid #dfe3e7; border-radius: 6px; padding: 10px 12px; background-color: #f7f9fb;">
      <div style="font-size: 22px; font-weight: bold; color: #0955abff;">1.00 → 0.11</div>
      <div style="font-size: 13px; color: #4a5158;">How the benefit of an honest helper collapses as the overseer gets stronger (critique protocol)</div>
    </div>
    <div style="flex: 1 1 150px; border: 1px solid #dfe3e7; border-radius: 6px; padding: 10px 12px; background-color: #f7f9fb;">
      <div style="font-size: 22px; font-weight: bold; color: #a32020;">100%</div>
      <div style="font-size: 13px; color: #4a5158;">False-positive rate when a lying helper tells the weak overseer a clean trajectory is flawed</div>
    </div>
  </div>

  <div style="flex: 1; display: flex;">
    <p style="margin: 0; padding: 4px 0; font-size: 15px;">
      <strong>The question.</strong> Scalable-oversight protocols - debate, consultancy, critique - rest on one assumption: that a weak overseer, given stronger assistants, can supervise work beyond its own unaided ability. This paper tests that assumption where it matters for AI agents, in which an overseer has to audit a multi-step tool-use trajectory rather than a single answer.
      <br><br>
      <strong>The setup.</strong> I built a deterministic records-analyst environment - a seeded 240-record database with query and calculator tools - and generated 560 labeled trajectories across 80 tasks (one clean, plus one of each of six flaw types). The flaw of interest is <em>fabricated_observation</em>: a returned value is altered and then propagated consistently through the rest of the trajectory. The result is internally coherent. The only evidence that anything is wrong lives in the environment, which a tool-blind overseer cannot reach.
      <br><br>
      <strong>What happened.</strong> The unaided overseer catches every flaw that is checkable from the trace - arithmetic errors, plan inconsistencies, broken chains, logged policy violations - and catches the fabricated observation <strong>0.00</strong> of the time. That number does not move with capability (Haiku, Sonnet, Opus alike), so the gap is structural, not a matter of the overseer being too weak.
      <br><br>
      Give a weak overseer an honest helper with ground truth, and detection jumps to ~1.00. That looks exactly like the amplification effect the literature predicts. It isn't.
    </p>
  </div>

  <!-- Table 1 -->
  <div style="overflow-x: auto; margin: 16px 0 6px 0;">
    <table style="border-collapse: collapse; width: 100%; font-size: 14px;">
      <thead>
        <tr style="background-color: #eef2f6;">
          <th style="border: 1px solid #cfd6dd; padding: 7px 10px; text-align: left;">Protocol</th>
          <th style="border: 1px solid #cfd6dd; padding: 7px 10px; text-align: left;">weak (Haiku)</th>
          <th style="border: 1px solid #cfd6dd; padding: 7px 10px; text-align: left;">mid (Sonnet)</th>
          <th style="border: 1px solid #cfd6dd; padding: 7px 10px; text-align: left;">strong (Opus)</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;"><strong>judge-alone</strong></td>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;">0.00 [0, .045]</td>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;">0.00 [0, .045]</td>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;">0.00 [0, .045]</td>
        </tr>
        <tr style="background-color: #fafbfc;">
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;"><strong>critique</strong></td>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;">1.00 [.955, 1]</td>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;">0.86 [0.79, 0.94]</td>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;">0.11 [0.05, 0.19]</td>
        </tr>
        <tr>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;"><strong>debate †</strong></td>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;">0.99 [0.96, 1.00]</td>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;">0.03 [0.00, 0.06]</td>
          <td style="border: 1px solid #cfd6dd; padding: 7px 10px;">0.00 [0, .045]</td>
        </tr>
      </tbody>
    </table>
  </div>
  <p style="margin: 0 0 14px 0; font-size: 13px; color: #6a7178; font-style: italic;">
    Fabricated_observation detection by protocol and overseer tier (n = 80 per cell). Saturated cells use exact Clopper-Pearson 95% intervals; others use a 2000-resample bootstrap. † Debate is a lower bound - an honest helper assigned to argue "clean" for a genuinely flawed item concedes rather than fabricate a defense, which degrades the protocol. Critique assigns no false side, so it carries the headline result.
  </p>

  <div style="flex: 1; display: flex;">
    <p style="margin: 0; padding: 4px 0; font-size: 15px;">
      <strong>Why the amplification is an illusion.</strong> Two results converge. First, the benefit decays monotonically as the overseer gets stronger - by the Opus tier, critique recovers almost nothing. Reading the transcripts shows why: the strong overseer reasons that it "must evaluate based on what it can observe, not on claims about a verification report or gold answer it cannot access," treats the helper's citation as unsupported assertion, rechecks the internally consistent arithmetic, and rules the item clean. It is not malfunctioning. It is applying exactly the right skepticism to a claim it cannot check.
      <br><br>
      Second, a <strong>lying-helper ablation</strong> makes the mechanism explicit. Feed the critique protocol a falsified report claiming a flaw in a <em>clean</em> trajectory, and the weak overseer flags all 80 out of 80 - no independent discrimination whatsoever, just echoing the assertion. That false-positive rate falls to 0.70 at mid and 0.20 at strong, tracking the honest-helper benefit almost step for step. The trust that lets assistance "help" is the same trust that makes the overseer foolable. They are not two properties. They are one.
      <br><br>
      <strong>Ruling out the obvious objection.</strong> Helpers are fixed at the mid tier, so the strong overseer outranks its helper - maybe it is discounting a weaker source, not an unverifiable claim. Capability parity at the mid tier yields 0.86, so the source-capability account predicts roughly that for a matched strong pair. Measured: <strong>0.18</strong> [0.11, 0.27], recovering 7 of the 75 percentage points lost, and not significantly different from the 0.11 baseline (p ≈ .26). Meanwhile a <em>stronger</em> lying helper pushes false positives up from 0.20 to 0.35 (p ≈ .03). Raising helper capability buys persuasion, not verification.
      <br><br>
      <strong>What follows.</strong> When the overseer cannot verify the evidence, amplification and gullibility are indistinguishable - accepting unverifiable claims helps on true ones and fails on false ones, and rejecting them does the reverse. Honest assistance cannot close a structural verification gap. Two things follow practically: any reported weak-overseer amplification should be published alongside a credulity control such as a lying-helper false-positive rate, and the real investment for agent oversight is in machinery that makes ground truth checkable - replayable tool execution, trusted verifiers, provenance on observations - rather than in more persuasive assistants.
    </p>
  </div>

  <div style="flex: 1;">
    <div style="display: flex; flex-wrap: wrap; gap: 12px; align-items: center; justify-content: space-between; margin-top: 10px; font-size: 15px;">
      <a href="/files/agent-oversight-credulity.pdf" style="color: #0955abff; text-decoration: none; font-weight: bold;">
        Read the Paper (PDF) →
      </a>
      <a href="/files/agent-oversight-credulity.pdf" download style="color: #0955abff; text-decoration: none; font-weight: bold;">
        Download PDF ↓
      </a>
      <a href="https://github.com/siliconshells/agent-oversight-credulity" target="_blank" style="color: #0366d6; text-decoration: none; font-weight: bold;">
        Code, Data &amp; Figures on GitHub →
      </a>
    </div>
  </div>

</div>
