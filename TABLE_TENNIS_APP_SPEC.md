# Table Tennis Match Tracker - Product Specification

## Overview
A cross-platform mobile app for table tennis players to track matches, maintain detailed opponent profiles with photos, and analyze playing patterns. Features a shared database allowing players to discover and learn from the community's knowledge about opponents.

## Core Features

### 1. Match Tracking

#### Match Creation
- Quick match start with minimal input required
- Select opponent from database or create new
- Match format: Standard ITTF rules (11 points, win by 2, best of 5 or 7 games)
- Record match location (optional)
- Record match date/time (auto-filled, editable)

#### Live Scoring
- Simple tap interface for point scoring
- **Landscape scoring mode** (recommended during live play):
  - Rotate phone horizontally for full-screen scoring interface
  - Split-screen layout: your score on left, opponent on right
  - Extra-large score numbers (easily visible from distance)
  - **Quick scoring gestures**:
    - Swipe up on your side = add point to you
    - Swipe up on opponent side = add point to opponent
    - Tap either side as alternative to swipe
  - Minimal UI - just scores, game count, and service indicator
  - Shake to undo last point (or swipe down)
  - Quick access menu button at bottom (for timeout, document rally, end game)
- Portrait mode also available with traditional button interface
- Visual score display with current game and overall match score
- Undo last point (for mistakes)
- Timeout tracking (1 timeout per player per match)
- Service indicator (alternates every 2 points, every point at 10-10)
- Game-by-game history displayed during match
- Quick "Document Rally" button to capture significant points with visual diagram

#### Match Results
- Automatic win detection
- Final score summary with game-by-game breakdown
- Option to add post-match notes
- Document key rallies from the match
- Quick rematch option
- Share match result (text/image, including rally diagrams)

### 2. Player Profiles

#### Personal Profile
- Profile photo with rubber type indicator badges
- Display name
- Playing hand (left/right)
- Playing style (offensive, defensive, all-around)
- Current equipment:
  - Blade
  - Forehand rubber (type and model)
    - Types: Inverted, Short Pips, Long Pips, Antispin
  - Backhand rubber (type and model)
    - Types: Inverted, Short Pips, Long Pips, Antispin
- **Rubber type visual indicators**: Small badges on avatar showing rubber configuration
  - Forehand indicator (left side of avatar)
  - Backhand indicator (right side of avatar)
  - **Visual patterns clearly distinguish rubber types**:
    - **Inverted**: Solid smooth red surface (standard high-spin rubber)
    - **Short Pips**: Orange with visible dot pattern (fast, less spin)
    - **Long Pips**: Purple with spike/star pattern (reverses spin, defensive)
    - **Antispin**: Gray with mesh/grid pattern (no spin, dead ball)
  - Patterns are visible even at small sizes (18-24px badges)
  - Hover tooltips show full rubber type name
- Rating/skill level (calculated from match history)
- Win/loss record
- Favorite shots/strengths

#### Opponent Profiles (Shared Database)
- All fields from personal profile
- Community-contributed information:
  - Equipment details (racket, rubbers)
  - Playing style notes
  - Serve characteristics (type, placement, spin)
  - Weakness identification
  - Strengths/patterns
  - Behavioral notes (mental game, under pressure, etc.)
- Photos (profile picture, optional action shots)
- Match history against this opponent (personal)
- Overall community stats for this opponent
- Edit/contribution history (who added what info)
- Verification badges for known players

### 3. Opponent Intelligence

#### Note Categories
- **Equipment**: Current and historical equipment usage
- **Serves**: Types, placement, spin variations, tells
- **Receive**: Return patterns, weaknesses
- **Forehand**: Characteristics, preferred shots, weaknesses
- **Backhand**: Characteristics, preferred shots, weaknesses
- **Footwork**: Movement patterns, coverage
- **Tactics**: Game plans, patterns under different scenarios
- **Mental**: Behavior under pressure, tilt triggers, composure
- **Physical**: Stamina, speed, reach
- **General**: Any other observations

#### Smart Features
- Tag-based notes (e.g., #longpips, #pendulumserve, #weakbackhand)
- Quick-add templates for common observations
- Attach rally diagrams to notes for visual examples
- Before-match summary of key notes to review (including relevant rally diagrams)
- Post-match prompt to add new observations

### 4. Statistics & Analytics

#### Personal Stats
- Overall win/loss record
- Win rate trend over time
- Performance by opponent playing style
- Performance by location
- Average points per game
- Game win percentage vs match win percentage
- Comeback statistics (matches won after losing first game, etc.)
- Longest winning/losing streaks

#### Opponent-Specific Stats
- Head-to-head record
- Point differential trends
- Game-by-game performance patterns
- Success rate of different strategies (if noted)

#### Community Stats
- Most played opponents
- Most documented opponents
- Rating/ranking system (ELO-style, optional)

### 5. Discovery & Social

#### Player Search
- Search by name
- Filter by location, playing style, skill level
- Recently played opponents
- Nearby players (location-based)
- Suggested opponents (based on skill level match)

#### Contribution System
- Reputation score for quality contributions
- Ability to upvote/downvote information accuracy
- Report incorrect or outdated information
- Edit suggestions with approval system
- Activity log of contributions

#### Privacy Controls
- Make personal profile public/private
- Choose which matches to make public
- Option to hide specific opponents from public view
- Control who can add notes to your profile

### 6. Rally Documentation & Tactical Diagrams

#### Visual Rally Builder
- Interactive table diagram (top-down view)
- Touch-based drawing tools:
  - Ball trajectory arrows (serve, return, subsequent shots)
  - Placement markers (where ball landed)
  - Player position indicators
  - Spin indicators (topspin, backspin, sidespin arrows)
  - Shot type labels (loop, push, smash, block, etc.)
- Color coding:
  - User's shots (e.g., blue)
  - Opponent's shots (e.g., red)
  - Serve marked distinctly
- Multi-stroke rally support (document entire rally sequence)

#### Drawing Tools
- Arrow tool: draw ball trajectory with drag gesture
- Tap to place: landing position markers
- Spin picker: select spin type for each shot
- Shot type picker: label shots (forehand loop, backhand push, etc.)
- Text annotation: add brief notes to specific shots
- Undo/redo functionality
- Clear all and start over
- Zoom in/out for precise placement

#### Table Diagram Features
- Regulation table proportions (9ft x 5ft)
- Net visualization
- Court position grid (optional overlay)
- Service zones marked
- Half-court lines
- Serving side indicator (right/left)

#### Rally Metadata
- Title/description of the rally
- When it occurred (match ID, game number, score at time)
- Outcome (who won the point)
- Tags (e.g., #breakpoint, #servingpattern, #weaknessexploited)
- Effectiveness rating (1-5 stars)
- Notes about what made this rally significant

#### Integration Points
- **During match**: Quick "Document Rally" button from live scoring
- **Post-match**: Add rallies when reviewing match
- **Opponent notes**: Attach rally diagrams to opponent profile as tactical examples
- **Playbook**: Save successful rally patterns to personal playbook
- **Community sharing**: Share rally diagrams to opponent profiles (with permission)

#### Rally Library
- Personal collection of documented rallies
- Filter by:
  - Opponent
  - Outcome (won/lost point)
  - Serve type
  - Tags
  - Date range
- Search by description or tags
- Group related rallies into "patterns" or "tactics"
- Compare similar rallies side-by-side

#### Use Cases
1. **Documenting effective serves**: Show exact placement and spin that gave you an ace
2. **Weakness exploitation**: Diagram the pattern that consistently scores against an opponent's backhand
3. **Problem-solving**: Document rallies you lost to analyze what went wrong
4. **Pattern recognition**: Build a library of successful rally patterns to reuse
5. **Coaching**: Share diagrams with coach or training partners
6. **Community knowledge**: Contribute effective tactics against specific opponents

#### Export & Sharing
- Save rally diagram as image
- Share to social media
- Export to PDF (multiple rallies)
- Add to opponent profile notes
- Print for offline review

### 7. Training Programs & Exercise Tracking

#### Training Program Builder
- Create custom training programs with multiple exercises
- Pre-built program templates:
  - **Beginner**: Basic stroke development, footwork fundamentals
  - **Intermediate**: Multi-ball drills, combination play, consistency training
  - **Advanced**: High-intensity patterns, match simulation, pressure training
  - **Specialized**: Serve practice, return of serve, loop training, counter-attack
- Set program duration (daily, weekly, custom schedule)
- Assign exercises to specific days/sessions
- Track completion and progress over time

#### Exercise Categories

**Table Tennis Drills:**
- **Multi-ball exercises**: Forehand loop, backhand push, random placement
- **Footwork patterns**: Side-to-side, pivot, triangle step, forward/backward
- **Serve practice**: Pendulum serve, reverse pendulum, tomahawk, high-toss
- **Return drills**: Against different spins, placement variations
- **Combination play**: Forehand-backhand sequences, serve-third ball
- **Match simulation**: Point-to-point play, pressure situations
- **Consistency training**: Rally count targets, no-miss drills

**Physical Training:**
- **Coordination**: Shadow play, reaction ball catches, agility ladder
- **Balance**: Single-leg stands, stability ball exercises, wobble board
- **Speed**: Sprint intervals, quick feet drills, explosive starts
- **Power**: Medicine ball throws, jump squats, resistance bands
- **Endurance**: Interval running, continuous footwork, stamina circuits
- **Flexibility**: Dynamic stretching, static holds, mobility work
- **Core strength**: Planks, Russian twists, anti-rotation exercises

#### Exercise Details
Each exercise includes:
- **Title**: Clear, descriptive name
- **Category**: Drill type or physical attribute targeted
- **Difficulty level**: Beginner, Intermediate, Advanced
- **Equipment needed**: Table, robot, partner, medicine ball, etc.
- **Target repetitions/sets/duration**: Configurable by user
- **Rest intervals**: Between sets or exercises
- **Visual illustration**:
  - Table tennis drills: Top-down table diagram showing ball placement and movement
  - Physical exercises: Stick figure illustrations or photos showing proper form
- **Step-by-step instructions**: Written guidance for execution
- **Key focus points**: What to concentrate on during exercise
- **Common mistakes**: What to avoid
- **Progression/regression**: Easier or harder variations
- **Demo video link**: (optional) Link to YouTube/external video

#### Visual Drill Illustrations

**Table Tennis Drills:**
- Interactive table diagram similar to rally documentation
- Show ball feeding pattern (for multi-ball)
- Player movement path with footwork arrows
- Target zones highlighted on table
- Shot trajectory arrows (loop, push, drive patterns)
- Coach/robot position indicator
- Repetition flow (exercise sequence visualization)

**Physical Exercises:**
- Side-view stick figure illustrations
- Movement phases (start → mid → end positions)
- Directional arrows showing motion
- Equipment positioning
- Body alignment guides
- Range of motion indicators

#### Training Session Tracking
- Start training session from program or ad-hoc
- Exercise-by-exercise checklist view
- Quick logging interface:
  - Check off completed exercises
  - Log actual reps/sets/duration performed
  - Rate difficulty (too easy, just right, too hard)
  - Add notes about performance or feelings
- Session timer (total time, per-exercise timing)
- Rest timer between sets
- Progressive overload tracking (weight, reps, speed increases)

#### Training History & Analytics
- **Session log**: Calendar view of completed training sessions
- **Completion rate**: % of scheduled workouts completed
- **Exercise frequency**: Most/least practiced exercises
- **Volume tracking**: Total reps, sets, duration over time
- **Strength progression**: Track improvements in physical exercises
- **Drill performance**: Hit rates, consistency scores (if tracked)
- **Training load**: Weekly/monthly volume trends
- **Consistency streaks**: Days/weeks of continuous training
- **Before/after comparisons**: Performance in matches after training periods

#### Exercise Library
- Browse all available exercises by category
- Search by equipment available
- Filter by difficulty level
- Sort by popularity or effectiveness
- Add to favorites for quick access
- Create custom exercises:
  - Add title, description, instructions
  - Draw custom drill diagrams
  - Upload photos/videos
  - Set default reps/sets
- Community-contributed exercises (with ratings)

#### Program Templates Library
Pre-built programs from coaches/pros:
- **"30-Day Footwork Foundation"**: Daily footwork drills progression
- **"Serve Mastery Program"**: 6-week serve development
- **"Tournament Prep"**: 2-week intensive pre-competition training
- **"Comeback Training"**: Gentle program for injury recovery
- **"Weekend Warrior"**: Efficient 2x/week program for busy players
- Community-shared programs (with reviews and completion rates)

#### Smart Features
- **Auto-progression**: Automatically increase difficulty when exercises become easy
- **Rest day reminders**: Suggest recovery when training volume is high
- **Deload weeks**: Built into longer programs for recovery
- **Match correlation**: See how training affects match performance
- **Exercise recommendations**: Suggest drills based on match weaknesses
- **Training reminders**: Push notifications for scheduled sessions
- **Partner finding**: Connect with others doing similar training

#### Integration Points
- **From match analysis**: "Your backhand push needs work" → Suggest backhand push drills
- **From opponent notes**: "Opponent has fast serves" → Suggest return-of-serve training
- **From rally library**: Convert rally diagrams into training drills
- **To stats**: Show correlation between training volume and win rate
- **Calendar sync**: Add training sessions to device calendar

#### Export & Sharing
- Share programs with training partners
- Export training log as PDF/CSV
- Print exercise cards for gym/table
- Share progress photos/videos to social
- Send program to coach for review

### 8. Photos & Media

#### Photo Features
- Profile photos (self and opponents)
- Action shot gallery (optional)
- Equipment photos (racket, rubbers)
- Photo upload from camera or gallery
- Basic cropping/editing tools
- Photo captions and tags

#### Storage & Quality
- Cloud storage for all photos
- Compressed for mobile performance
- Original quality preserved for zoom

## Technical Requirements

### Platform
- Cross-platform mobile app (React Native or Flutter recommended)
- iOS 14+ and Android 8+ support
- Responsive design for tablets

### Backend
- Cloud-based backend (Firebase, Supabase, or custom API)
- Real-time sync for shared database
- RESTful API architecture
- User authentication (email/password, social logins)

### Data Model

#### Users
- User ID (unique)
- Email, password hash
- Profile information
- Settings/preferences
- Created/updated timestamps

#### Players (Opponent profiles in shared database)
- Player ID (unique)
- Basic profile fields
- Equipment information
- Community-contributed notes
- Statistics aggregates
- Photo references
- Verification status

#### Matches
- Match ID
- User ID (who recorded)
- Opponent Player ID
- Match date/time/location
- Game-by-game scores
- Total match time
- Notes
- Public/private flag

#### Notes
- Note ID
- Player ID (subject)
- User ID (author)
- Category
- Content
- Tags
- Upvotes/downvotes
- Timestamps

#### Photos
- Photo ID
- Uploader User ID
- Subject Player ID
- Photo URL
- Caption
- Tags
- Upload timestamp

#### Rally Diagrams
- Rally ID (unique)
- User ID (creator)
- Match ID (optional, if from specific match)
- Opponent Player ID
- Title/description
- Diagram data (JSON):
  - Shot sequence array (coordinates, type, spin, player)
  - Landing positions
  - Annotations
  - Table orientation
- Outcome (won/lost point)
- Tags
- Effectiveness rating
- Public/private flag
- Upvotes/downvotes (if shared to community)
- Created/updated timestamps
- Associated notes/context

### Security & Privacy
- User authentication required
- Row-level security for private data
- Rate limiting on API requests
- Content moderation for shared profiles
- GDPR compliance (right to deletion, data export)
- Inappropriate content reporting system

## User Experience

### Onboarding
1. Create account (email or social)
2. Set up personal profile (name, photo, playing hand, style)
3. Optional tutorial showing key features
4. Prompt to record first match

### Primary User Flows

#### Flow 1: Recording a Match
1. Tap "New Match" from home screen
2. Select/search for opponent or create new
3. Quick review of opponent notes (if available)
4. Confirm match format (best of 5/7)
5. Live scoring interface
6. Match complete, view summary
7. Prompt to add notes about opponent performance

#### Flow 2: Researching an Opponent
1. Search for opponent by name
2. View profile with photo and basic info
3. Review community notes organized by category
4. Check head-to-head history if previously played
5. Add to favorites or take notes for preparation

#### Flow 3: Contributing Knowledge
1. Navigate to opponent profile
2. Select "Add Note" or edit existing section
3. Choose category
4. Write observation with optional tags
5. Submit for community review (or immediate post if high reputation)

#### Flow 4: Documenting a Rally
1. During/after match, tap "Document Rally"
2. Interactive table diagram appears
3. Draw serve trajectory with finger (arrow appears)
4. Tap opponent's return position, draw return arrow
5. Continue sequence for entire rally
6. Add shot type labels and spin indicators
7. Add title and tags
8. Save to personal library or attach to opponent profile

#### Flow 5: Creating and Following a Training Program
1. Navigate to Training tab
2. Choose "Create Program" or select from templates
3. Add exercises from library (browse by category or search)
4. Customize reps/sets/duration for each exercise
5. Set schedule (which days, how many weeks)
6. Save program and set reminders
7. On training day, start session from program
8. Follow exercise-by-exercise with visual guides
9. Check off completed exercises and log performance
10. View progress and statistics over time

### Home Screen
- Quick "New Match" button (primary action)
- Recent matches list
- Upcoming scheduled matches (future feature)
- Quick stats summary (current streak, W/L ratio)
- Search opponents button
- Notifications badge

### Navigation
- Bottom tab bar:
  - Home
  - Matches (history)
  - Training (programs & exercises)
  - Discover (search opponents)
  - Stats
  - Profile (personal)

## Future Enhancements (V2+)
- Video recording and annotation
- Club/team management features
- Tournament bracket management
- Match scheduling and invites
- In-app messaging
- Coach mode (coaching multiple players)
- Integration with smart scoring devices
- AI-powered pattern recognition from match data
- Practice partner matching
- Equipment marketplace/recommendations
- Multi-language support

## Success Metrics
- Daily active users
- Matches recorded per user per week
- Training sessions completed per user per week
- Training program completion rate
- Opponent profiles with >5 detailed notes
- User retention (30-day, 90-day)
- Time from account creation to first match recorded
- Community contribution rate (% of users who add notes)
- Photo upload rate
- Rally diagrams created per user per week
- Rally diagrams shared to community
- Rally diagrams attached to opponent profiles
- Custom exercises created by users
- Community training programs created and shared
- Correlation between training volume and win rate improvement

## Open Questions for Discussion
1. Should there be a freemium model or paid features?
2. How to handle duplicate player profiles (same person, multiple entries)?
3. Should match history be completely public or require connections?
4. Moderation approach for shared database (automated, community, staff)?
5. Should we support doubles matches in V1 or defer to V2?
6. Equipment database: free-form text or structured database of known products?
7. Rating system: mandatory or optional? Algorithm choice?
8. Real-time scoring sync for matches (both players can enter scores)?
