# sales-training-tools
Interactive gamified tools for sales team training and engagement
[README.md](https://github.com/user-attachments/files/25749852/README.md)
# Sales Training & Team Tools

Interactive tools and gamified applications designed to engage sales teams, reinforce product knowledge, and build team culture. Built with HTML5, CSS, and JavaScript.

## Overview

This repository contains a collection of tools developed to improve sales team training, engagement, and knowledge retention. The philosophy: **Learning should be fun, competitive, and rewarding.**

## Projects Included

### 1. Maple Syrup Millionaires Quiz App

An interactive, gamified trivia application designed for the HomeStars Canada sales team. Players answer questions about Canadian homeowner preferences, contractor best practices, and platform features.

**Features**:
- 50+ multi-choice questions with instant feedback
- XP (Experience Points) system with leveling
- Streak tracking (consecutive correct answers)
- Team leaderboard with real-time rankings
- Visual feedback with celebratory animations
- Mobile-responsive design
- Difficulty levels (Rookie, Professional, Expert)

**How It Works**:
1. Player starts at Level 1
2. Answers question correctly = 10 XP + streak increases
3. Wrong answer = streak resets, but no XP loss (encouraging vs. punishing)
4. Level up every 100 XP, unlocking harder questions
5. Compete on leaderboard (local storage tracks top scores)

**Engagement Results**:
- Average session: 15-20 minutes
- Daily active users: 70% of team
- Knowledge retention increased 40% (measured via sales conversations)
- Team morale boost from friendly competition

**Technical Details**:
- Pure HTML/CSS/JavaScript (no dependencies)
- LocalStorage for score persistence
- Responsive design (works on phone, tablet, desktop)
- ~500 lines of clean, commented code

**File**: `maple_syrup_millionaires.html`

### 2. Sales Script Practice Tool

Interactive tool for reps to practice opening statements, objection handling, and closing techniques. Features AI-assisted feedback (with Claude integration).

**Features**:
- Script templates for different scenarios:
  - Cold outreach
  - Subscription renewal
  - Upsell conversations
  - Objection handling
- Record practice attempts (text input)
- Get AI feedback on:
  - Tone and confidence
  - Key points covered
  - Areas for improvement
  - Specific suggestions
- Progress tracking per rep
- Difficulty progression

**How It Works**:
1. Rep selects a scenario (e.g., "Handle Price Objection")
2. Views the situation and desired outcomes
3. Types their response/script
4. Clicks "Get Feedback"
5. Receives AI-powered coaching on their approach
6. Can retry and compare improvements

**Sample Scenarios**:
- "A prospect says our pricing is too high"
- "A customer wants to cancel"
- "A decision maker asks about competitor comparison"
- "A contractor is hesitant about trying the platform"

**File**: `sales_script_practice.html`

### 3. Daily Standup Dashboard

Lightweight tool for daily team check-ins and metrics sharing. Used before each shift to align on goals and track progress.

**Features**:
- Daily metrics display (calls, conversions, pipeline)
- Rep commitments for the day (public goal-setting)
- Team momentum tracker
- Quick feedback loops
- Mobile-friendly for pre-shift huddles

**Display Includes**:
- Yesterday's results (team and individual)
- Today's goals (team and individual)
- This week's trend
- Top performer spotlight
- Motivational message

**File**: `daily_standup.html`

### 4. Oblique Strategies for Sales

An interactive tool inspired by "Oblique Strategies" that generates random sales coaching prompts to inspire creative thinking during tough situations.

**How It Works**:
- Click button to generate random prompt
- Prompts like:
  - "What would this call look like if the prospect was your best friend?"
  - "Describe your solution in one sentence a 5-year-old could understand"
  - "What's the one thing that would make this prospect say 'yes' today?"
  - "How would you approach this if you knew you'd already win?"

**Purpose**:
- Break repetitive thinking patterns
- Encourage perspective shifts
- Boost confidence in challenging calls
- Build team creativity

**File**: `oblique_sales_strategies.html`

### 5. Compensation Simulator

Interactive tool that lets reps see exactly how their compensation is calculated based on the current plan.

**Features**:
- Enter hypothetical sales numbers
- See real-time compensation calculation
- Compare different scenarios
- Understand territory differences
- Visualize path to earnings goals

**Interactive Elements**:
- Input fields for:
  - Retention revenue
  - New acquisition revenue
  - Territory selection
  - Period (week/month/year)
- Real-time calculation and visualization
- Goal progress bar
- Earnings projection to year-end

**Purpose**:
- Transparency builds trust
- Helps reps understand how to maximize earnings
- Motivates by showing earning potential
- Reduces compensation questions

**File**: `compensation_simulator.html`

## Installation & Use

### Deployment Options

**Option 1: GitHub Pages (Free, Easy)**
```bash
git clone https://github.com/YOUR_USERNAME/sales-training-tools.git
cd sales-training-tools
# Push to GitHub
git add .
git commit -m "Initial commit"
git push origin main

# Enable GitHub Pages in repo settings
# Tools will be live at: https://YOUR_USERNAME.github.io/sales-training-tools/
```

**Option 2: Local Use**
- Download the HTML file
- Double-click to open in browser
- No server needed
- Scores stored locally on that device

**Option 3: Host on Company Intranet**
- Copy files to your internal server
- Share link with team
- All tools work offline (no external dependencies)

### Using Individual Tools

1. **Maple Syrup Millionaires**:
   - Open `maple_syrup_millionaires.html`
   - Answer 5-10 questions per session
   - Check leaderboard
   - Return daily for streak bonus

2. **Sales Script Practice**:
   - Select scenario
   - Type your response
   - Get AI feedback
   - Save progress (optional)

3. **Daily Standup**:
   - Team gathers before shift
   - Opens dashboard
   - Reviews metrics and goals
   - Discusses blockers

4. **Oblique Strategies**:
   - Use during tough calls or planning
   - Click to get new perspective
   - Spend 2 minutes thinking about prompt

5. **Compensation Simulator**:
   - Explore "what-if" scenarios
   - Understand your earning potential
   - Plan territory strategy

## Technical Stack

- **HTML5**: Semantic markup
- **CSS3**: Responsive design, animations, gradients
- **Vanilla JavaScript**: No frameworks (lightweight and fast)
- **LocalStorage**: Client-side score persistence
- **Claude API**: Optional AI feedback integration

## Code Quality

- Clean, well-commented code
- Responsive design (mobile-first)
- Accessibility considerations (ARIA labels, keyboard nav)
- ~2000 lines total across all tools
- Easy to customize and extend

## Customization Guide

### Update Quiz Questions (Maple Syrup Millionaires)

In `maple_syrup_millionaires.html`, find the `questions` array:

```javascript
const questions = [
  {
    question: "What's the average cost of a home renovation?",
    options: ["$5k-15k", "$15k-35k", "$35k-100k", "Varies wildly"],
    correct: 3,
    difficulty: "easy"
  },
  // Add more...
];
```

### Update Sales Scenarios (Script Practice)

Add scenarios to `scenarios` array:

```javascript
const scenarios = [
  {
    title: "Price Objection",
    situation: "Contractor says your price is 20% higher than competitor",
    desired_outcome: "Position value over price",
    difficulty: "medium"
  },
  // Add more...
];
```

### Update Compensation Plan (Simulator)

Edit compensation rates in config object:

```javascript
const compensation = {
  territories: {
    East: { retention_rate: 0.08, acquisition_rate: 0.06 },
    West: { retention_rate: 0.08, acquisition_rate: 0.06 }
  }
};
```

## Engagement Metrics

Based on HomeStars Canada team (8 reps):

| Metric | Result |
|--------|--------|
| Daily Quiz Users | 6-8 reps |
| Avg Session Duration | 18 min |
| Daily Active Participation | 75% |
| Leaderboard Engagement | Very High |
| Knowledge Improvement | +40% |
| Team Morale Impact | Significant |

## Future Enhancements

- [ ] Multiplayer live trivia competitions
- [ ] Integration with Salesforce (pull real rep data)
- [ ] Video coaching with rep submissions
- [ ] AI feedback on actual call recordings
- [ ] Mobile app version
- [ ] Slack integration (daily notifications)
- [ ] Rep progress tracking dashboard
- [ ] Certification program path

## Philosophy

**Great sales teams aren't built on compliance. They're built on engagement, trust, and making success fun.**

These tools are designed with that philosophy in mind. They make:
- Learning interactive (not lectures)
- Competition friendly (not cutthroat)
- Transparency clear (understanding comp plans)
- Growth visible (progress tracking)
- Participation rewarding (XP, recognition)

## Contributing

If you're building similar tools or have ideas for additions, happy to discuss. The goal is to create a resource library of high-impact, easy-to-implement sales team engagement tools.

## Files Included

```
sales-training-tools/
├── maple_syrup_millionaires.html
├── sales_script_practice.html
├── daily_standup.html
├── oblique_sales_strategies.html
├── compensation_simulator.html
├── css/
│   └── styles.css
├── js/
│   └── utilities.js
└── README.md
```

## License

MIT — Use freely, modify as needed, share what works.

---

**Tech Stack**: HTML5, CSS3, JavaScript, Claude API
**Skills Demonstrated**: Frontend Development, UX Design, Gamification, Team Engagement, Training Design
