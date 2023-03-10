# qtec-count-frequency

  $pattern_length = strlen($pattern);
  $text_length = strlen($text);
  $frequency = 0;

  // A loop to slide pattern[] one by one 
  for ($i = 0; $i <= $text_length - $pattern_length; $i++){
      // For current index i, check for pattern match
      for ($j = 0; $j < $pattern_length; $j++)
          if ($text[$i+$j] != $pattern[$j])
              break;

      // if pattern[0...pattern_length-1] = text[i, i+1, ...i+pattern_length-1]
      if ($j == $pattern_length){
          $frequency++;
          $j = 0;
      }
  }

