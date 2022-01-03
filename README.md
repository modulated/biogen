# Biogen
Life sim in Rust with ECS experiment

## Entities
### Creatures
- mobile or non-mobile
- need to eat or if their health reaches 0 they die
- lose 1 health per tick

### Food
- randomly appear on the map

## Components

### Position
- x: i64 
- y: i64

### RandomMover
- f: f64

### Health
- h: u64

### Nutrition
- n: u64

## Systems

### Hunger
- decrease Health component by 1 each tick

### RandomMover
- move in a random direction every tick at specified frequency (ie 0.0 = never move, 1.0 = always move)

### Eat
- if creature on food eat it and increase health by nutrition value

### FoodSpawner
- spawn food at specified rate randomly on map with random range of nutrition values

### Reproducer
- if health greater than cutoff split creature in 2
