/ # Dataset Columns – UCI Bike Sharing (hour.csv)

Source: Capital Bikeshare, Washington D.C., 2011–2012. Each row is one hour.

| Column | Description | Values |
|---|---|---|
| `instant` | Row index | 1, 2, 3, ... |
| `dteday` | Date | YYYY-MM-DD |
| `season` | Season | 1 = spring, 2 = summer, 3 = fall, 4 = winter |
| `yr` | Year | 0 = 2011, 1 = 2012 |
| `mnth` | Month | 1–12 |
| `hr` | Hour of the day | 0–23 |
| `holiday` | Public holiday | 0 = no, 1 = yes |
| `weekday` | Day of the week | 0 = Sunday ... 6 = Saturday |
| `workingday` | Working day (not weekend or holiday) | 0 = no, 1 = yes |
| `weathersit` | Weather situation | 1 = clear, 2 = mist/cloudy, 3 = light rain/snow, 4 = heavy rain/snow |
| `temp` | Temperature (normalised) | Celsius ÷ 41 |
| `atemp` | "Feels like" temperature (normalised) | Celsius ÷ 50 |
| `hum` | Humidity (normalised) | % ÷ 100 |
| `windspeed` | Wind speed (normalised) | value ÷ 67 |
| `casual` | Rentals by casual users | count |
| `registered` | Rentals by registered users | count |
| `cnt` | **Total rentals (target variable)** | casual + registered |

## Notes
- `cnt` is what we want to predict.
- `casual` and `registered` must **not** be used as features: they add up to `cnt`, which would leak the answer into the model.
- `instant` is just an index and has no predictive meaning.
