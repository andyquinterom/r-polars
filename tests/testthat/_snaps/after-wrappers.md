# public and private functions in pl and .pr

    Code
      ls(pl)
    Output
        [1] "Array"                     "Binary"                   
        [3] "Boolean"                   "Categorical"              
        [5] "DataFrame"                 "Date"                     
        [7] "Datetime"                  "Duration"                 
        [9] "Field"                     "Float32"                  
       [11] "Float64"                   "Int16"                    
       [13] "Int32"                     "Int64"                    
       [15] "Int8"                      "LazyFrame"                
       [17] "List"                      "Null"                     
       [19] "PTime"                     "SQLContext"               
       [21] "Series"                    "String"                   
       [23] "Struct"                    "Time"                     
       [25] "UInt16"                    "UInt32"                   
       [27] "UInt64"                    "UInt8"                    
       [29] "Unknown"                   "Utf8"                     
       [31] "all"                       "all_horizontal"           
       [33] "any_horizontal"            "approx_n_unique"          
       [35] "arg_sort_by"               "arg_where"                
       [37] "class_names"               "coalesce"                 
       [39] "col"                       "concat"                   
       [41] "concat_list"               "concat_str"               
       [43] "corr"                      "count"                    
       [45] "cov"                       "date"                     
       [47] "date_range"                "date_ranges"              
       [49] "datetime"                  "datetime_range"           
       [51] "datetime_ranges"           "disable_string_cache"     
       [53] "dtypes"                    "duration"                 
       [55] "element"                   "enable_string_cache"      
       [57] "first"                     "fold"                     
       [59] "from_epoch"                "get_global_rpool_cap"     
       [61] "head"                      "implode"                  
       [63] "int_range"                 "int_ranges"               
       [65] "is_schema"                 "last"                     
       [67] "len"                       "lit"                      
       [69] "max"                       "max_horizontal"           
       [71] "mean"                      "mean_horizontal"          
       [73] "median"                    "mem_address"              
       [75] "min"                       "min_horizontal"           
       [77] "n_unique"                  "numeric_dtypes"           
       [79] "raw_list"                  "read_csv"                 
       [81] "read_ipc"                  "read_ndjson"              
       [83] "read_parquet"              "reduce"                   
       [85] "rolling_corr"              "rolling_cov"              
       [87] "same_outer_dt"             "scan_csv"                 
       [89] "scan_ipc"                  "scan_ndjson"              
       [91] "scan_parquet"              "select"                   
       [93] "set_global_rpool_cap"      "show_all_public_functions"
       [95] "show_all_public_methods"   "std"                      
       [97] "struct"                    "sum"                      
       [99] "sum_horizontal"            "tail"                     
      [101] "thread_pool_size"          "time"                     
      [103] "using_string_cache"        "var"                      
      [105] "when"                      "with_string_cache"        

---

    Code
      ls(.pr)
    Output
       [1] "ChainedThen"       "ChainedWhen"       "DataFrame"        
       [4] "DataType"          "DataTypeVector"    "Err"              
       [7] "Expr"              "GroupBy"           "LazyFrame"        
      [10] "LazyGroupBy"       "RField"            "RNullValues"      
      [13] "RThreadHandle"     "SQLContext"        "Series"           
      [16] "StringCacheHolder" "Then"              "VecDataFrame"     
      [19] "When"              "env"               "print_env"        

# public and private methods of each class DataFrame

    Code
      ls(.pr$env[[class_name]])
    Output
       [1] "clear"            "clone"            "columns"          "describe"        
       [5] "drop"             "drop_in_place"    "drop_nulls"       "dtype_strings"   
       [9] "dtypes"           "equals"           "estimated_size"   "explode"         
      [13] "fill_nan"         "fill_null"        "filter"           "first"           
      [17] "flags"            "get_column"       "get_columns"      "glimpse"         
      [21] "group_by"         "group_by_dynamic" "head"             "height"          
      [25] "item"             "join"             "join_asof"        "last"            
      [29] "lazy"             "limit"            "max"              "mean"            
      [33] "median"           "melt"             "min"              "n_chunks"        
      [37] "null_count"       "partition_by"     "pivot"            "print"           
      [41] "quantile"         "rechunk"          "rename"           "reverse"         
      [45] "rolling"          "sample"           "schema"           "select"          
      [49] "select_seq"       "shape"            "shift"            "shift_and_fill"  
      [53] "slice"            "sort"             "std"              "sum"             
      [57] "tail"             "to_data_frame"    "to_list"          "to_series"       
      [61] "to_struct"        "transpose"        "unique"           "unnest"          
      [65] "var"              "width"            "with_columns"     "with_columns_seq"
      [69] "with_row_index"   "write_csv"        "write_ipc"        "write_json"      
      [73] "write_ndjson"     "write_parquet"   

---

    Code
      ls(.pr[[private_key]])
    Output
       [1] "clear"                     "clone_in_rust"            
       [3] "columns"                   "default"                  
       [5] "drop_all_in_place"         "drop_in_place"            
       [7] "dtype_strings"             "dtypes"                   
       [9] "equals"                    "estimated_size"           
      [11] "export_stream"             "from_arrow_record_batches"
      [13] "get_column"                "get_columns"              
      [15] "lazy"                      "melt"                     
      [17] "n_chunks"                  "new_with_capacity"        
      [19] "null_count"                "partition_by"             
      [21] "pivot_expr"                "print"                    
      [23] "rechunk"                   "sample_frac"              
      [25] "sample_n"                  "schema"                   
      [27] "select"                    "select_at_idx"            
      [29] "select_seq"                "set_column_from_robj"     
      [31] "set_column_from_series"    "set_column_names_mut"     
      [33] "shape"                     "to_list"                  
      [35] "to_list_tag_structs"       "to_list_unwind"           
      [37] "to_struct"                 "transpose"                
      [39] "unnest"                    "with_columns"             
      [41] "with_columns_seq"          "with_row_index"           
      [43] "write_csv"                 "write_ipc"                
      [45] "write_json"                "write_ndjson"             
      [47] "write_parquet"            

# public and private methods of each class GroupBy

    Code
      ls(.pr$env[[class_name]])
    Output
       [1] "agg"            "columns"        "first"          "last"          
       [5] "max"            "mean"           "median"         "min"           
       [9] "null_count"     "quantile"       "shift"          "shift_and_fill"
      [13] "std"            "sum"            "ungroup"        "var"           

# public and private methods of each class LazyFrame

    Code
      ls(.pr$env[[class_name]])
    Output
       [1] "clear"                   "clone"                  
       [3] "collect"                 "collect_in_background"  
       [5] "columns"                 "describe_optimized_plan"
       [7] "describe_plan"           "drop"                   
       [9] "drop_nulls"              "dtypes"                 
      [11] "explode"                 "fetch"                  
      [13] "fill_nan"                "fill_null"              
      [15] "filter"                  "first"                  
      [17] "get_optimization_toggle" "group_by"               
      [19] "group_by_dynamic"        "head"                   
      [21] "join"                    "join_asof"              
      [23] "last"                    "limit"                  
      [25] "max"                     "mean"                   
      [27] "median"                  "melt"                   
      [29] "min"                     "print"                  
      [31] "profile"                 "quantile"               
      [33] "rename"                  "reverse"                
      [35] "rolling"                 "schema"                 
      [37] "select"                  "select_seq"             
      [39] "set_optimization_toggle" "shift"                  
      [41] "shift_and_fill"          "sink_csv"               
      [43] "sink_ipc"                "sink_ndjson"            
      [45] "sink_parquet"            "slice"                  
      [47] "sort"                    "std"                    
      [49] "sum"                     "tail"                   
      [51] "to_dot"                  "unique"                 
      [53] "unnest"                  "var"                    
      [55] "width"                   "with_columns"           
      [57] "with_columns_seq"        "with_context"           
      [59] "with_row_index"         

---

    Code
      ls(.pr[[private_key]])
    Output
       [1] "clone_in_rust"           "collect"                
       [3] "collect_in_background"   "debug_plan"             
       [5] "describe_optimized_plan" "describe_plan"          
       [7] "drop"                    "drop_nulls"             
       [9] "explode"                 "fetch"                  
      [11] "fill_nan"                "fill_null"              
      [13] "filter"                  "first"                  
      [15] "get_optimization_toggle" "group_by"               
      [17] "group_by_dynamic"        "join"                   
      [19] "join_asof"               "last"                   
      [21] "max"                     "mean"                   
      [23] "median"                  "melt"                   
      [25] "min"                     "print"                  
      [27] "profile"                 "quantile"               
      [29] "rename"                  "reverse"                
      [31] "rolling"                 "schema"                 
      [33] "select"                  "select_seq"             
      [35] "set_optimization_toggle" "shift"                  
      [37] "shift_and_fill"          "sink_csv"               
      [39] "sink_ipc"                "sink_json"              
      [41] "sink_parquet"            "slice"                  
      [43] "sort_by_exprs"           "std"                    
      [45] "sum"                     "tail"                   
      [47] "to_dot"                  "unique"                 
      [49] "unnest"                  "var"                    
      [51] "with_columns"            "with_columns_seq"       
      [53] "with_context"            "with_row_index"         

# public and private methods of each class Expr

    Code
      ls(.pr$env[[class_name]])
    Output
        [1] "abs"               "add"               "agg_groups"       
        [4] "alias"             "all"               "and"              
        [7] "any"               "append"            "approx_n_unique"  
       [10] "arccos"            "arccosh"           "arcsin"           
       [13] "arcsinh"           "arctan"            "arctanh"          
       [16] "arg_max"           "arg_min"           "arg_sort"         
       [19] "arg_unique"        "arr"               "backward_fill"    
       [22] "bin"               "bottom_k"          "cast"             
       [25] "cat"               "ceil"              "clip"             
       [28] "clip_max"          "clip_min"          "cos"              
       [31] "cosh"              "count"             "cum_count"        
       [34] "cum_max"           "cum_min"           "cum_prod"         
       [37] "cum_sum"           "cumulative_eval"   "diff"             
       [40] "div"               "dot"               "drop_nans"        
       [43] "drop_nulls"        "dt"                "entropy"          
       [46] "eq"                "eq_missing"        "ewm_mean"         
       [49] "ewm_std"           "ewm_var"           "exclude"          
       [52] "exp"               "explode"           "extend_constant"  
       [55] "fill_nan"          "fill_null"         "filter"           
       [58] "first"             "flatten"           "floor"            
       [61] "floor_div"         "forward_fill"      "gather"           
       [64] "gather_every"      "gt"                "gt_eq"            
       [67] "hash"              "head"              "implode"          
       [70] "inspect"           "interpolate"       "is_between"       
       [73] "is_duplicated"     "is_finite"         "is_first_distinct"
       [76] "is_in"             "is_infinite"       "is_last_distinct" 
       [79] "is_nan"            "is_not_nan"        "is_not_null"      
       [82] "is_null"           "is_unique"         "kurtosis"         
       [85] "last"              "len"               "limit"            
       [88] "list"              "log"               "log10"            
       [91] "lower_bound"       "lt"                "lt_eq"            
       [94] "map_batches"       "map_elements"      "max"              
       [97] "mean"              "median"            "meta"             
      [100] "min"               "mod"               "mode"             
      [103] "mul"               "n_unique"          "name"             
      [106] "nan_max"           "nan_min"           "neq"              
      [109] "neq_missing"       "not"               "null_count"       
      [112] "or"                "over"              "pct_change"       
      [115] "peak_max"          "peak_min"          "pow"              
      [118] "print"             "product"           "quantile"         
      [121] "rank"              "rechunk"           "reinterpret"      
      [124] "rep"               "repeat_by"         "replace"          
      [127] "reshape"           "reverse"           "rle"              
      [130] "rle_id"            "rolling"           "rolling_max"      
      [133] "rolling_mean"      "rolling_median"    "rolling_min"      
      [136] "rolling_quantile"  "rolling_skew"      "rolling_std"      
      [139] "rolling_sum"       "rolling_var"       "round"            
      [142] "sample"            "search_sorted"     "set_sorted"       
      [145] "shift"             "shift_and_fill"    "shrink_dtype"     
      [148] "shuffle"           "sign"              "sin"              
      [151] "sinh"              "skew"              "slice"            
      [154] "sort"              "sort_by"           "sqrt"             
      [157] "std"               "str"               "struct"           
      [160] "sub"               "sum"               "tail"             
      [163] "tan"               "tanh"              "to_physical"      
      [166] "to_r"              "to_series"         "to_struct"        
      [169] "top_k"             "unique"            "unique_counts"    
      [172] "upper_bound"       "value_counts"      "var"              
      [175] "xor"              

---

    Code
      ls(.pr[[private_key]])
    Output
        [1] "abs"                        "add"                       
        [3] "agg_groups"                 "alias"                     
        [5] "all"                        "and"                       
        [7] "any"                        "append"                    
        [9] "approx_n_unique"            "arccos"                    
       [11] "arccosh"                    "arcsin"                    
       [13] "arcsinh"                    "arctan"                    
       [15] "arctanh"                    "arg_max"                   
       [17] "arg_min"                    "arg_sort"                  
       [19] "arg_unique"                 "arr_all"                   
       [21] "arr_any"                    "arr_arg_max"               
       [23] "arr_arg_min"                "arr_contains"              
       [25] "arr_count_matches"          "arr_get"                   
       [27] "arr_join"                   "arr_max"                   
       [29] "arr_median"                 "arr_min"                   
       [31] "arr_reverse"                "arr_shift"                 
       [33] "arr_sort"                   "arr_std"                   
       [35] "arr_sum"                    "arr_to_list"               
       [37] "arr_to_struct"              "arr_unique"                
       [39] "arr_var"                    "backward_fill"             
       [41] "bin_base64_decode"          "bin_base64_encode"         
       [43] "bin_contains"               "bin_ends_with"             
       [45] "bin_hex_decode"             "bin_hex_encode"            
       [47] "bin_starts_with"            "bottom_k"                  
       [49] "cast"                       "cat_get_categories"        
       [51] "cat_set_ordering"           "ceil"                      
       [53] "clip"                       "clip_max"                  
       [55] "clip_min"                   "col"                       
       [57] "cols"                       "corr"                      
       [59] "cos"                        "cosh"                      
       [61] "count"                      "cov"                       
       [63] "cum_count"                  "cum_max"                   
       [65] "cum_min"                    "cum_prod"                  
       [67] "cum_sum"                    "cumulative_eval"           
       [69] "diff"                       "div"                       
       [71] "dot"                        "drop_nans"                 
       [73] "drop_nulls"                 "dt_cast_time_unit"         
       [75] "dt_combine"                 "dt_convert_time_zone"      
       [77] "dt_day"                     "dt_epoch_seconds"          
       [79] "dt_hour"                    "dt_iso_year"               
       [81] "dt_microsecond"             "dt_millisecond"            
       [83] "dt_minute"                  "dt_month"                  
       [85] "dt_nanosecond"              "dt_offset_by"              
       [87] "dt_ordinal_day"             "dt_quarter"                
       [89] "dt_replace_time_zone"       "dt_round"                  
       [91] "dt_second"                  "dt_strftime"               
       [93] "dt_time"                    "dt_total_days"             
       [95] "dt_total_hours"             "dt_total_microseconds"     
       [97] "dt_total_milliseconds"      "dt_total_minutes"          
       [99] "dt_total_nanoseconds"       "dt_total_seconds"          
      [101] "dt_truncate"                "dt_week"                   
      [103] "dt_weekday"                 "dt_with_time_unit"         
      [105] "dt_year"                    "dtype_cols"                
      [107] "entropy"                    "eq"                        
      [109] "eq_missing"                 "ewm_mean"                  
      [111] "ewm_std"                    "ewm_var"                   
      [113] "exclude"                    "exclude_dtype"             
      [115] "exp"                        "explode"                   
      [117] "extend_constant"            "fill_nan"                  
      [119] "fill_null"                  "fill_null_with_strategy"   
      [121] "filter"                     "first"                     
      [123] "flatten"                    "floor"                     
      [125] "floor_div"                  "forward_fill"              
      [127] "gather"                     "gather_every"              
      [129] "gt"                         "gt_eq"                     
      [131] "hash"                       "head"                      
      [133] "implode"                    "interpolate"               
      [135] "is_between"                 "is_duplicated"             
      [137] "is_finite"                  "is_first_distinct"         
      [139] "is_in"                      "is_infinite"               
      [141] "is_last_distinct"           "is_nan"                    
      [143] "is_not_nan"                 "is_not_null"               
      [145] "is_null"                    "is_unique"                 
      [147] "kurtosis"                   "last"                      
      [149] "len"                        "list_all"                  
      [151] "list_any"                   "list_arg_max"              
      [153] "list_arg_min"               "list_contains"             
      [155] "list_diff"                  "list_eval"                 
      [157] "list_gather"                "list_gather_every"         
      [159] "list_get"                   "list_join"                 
      [161] "list_len"                   "list_max"                  
      [163] "list_mean"                  "list_min"                  
      [165] "list_n_unique"              "list_reverse"              
      [167] "list_set_operation"         "list_shift"                
      [169] "list_slice"                 "list_sort"                 
      [171] "list_sum"                   "list_to_struct"            
      [173] "list_unique"                "lit"                       
      [175] "log"                        "log10"                     
      [177] "lower_bound"                "lt"                        
      [179] "lt_eq"                      "map_batches"               
      [181] "map_batches_in_background"  "map_elements_in_background"
      [183] "max"                        "mean"                      
      [185] "median"                     "meta_eq"                   
      [187] "meta_has_multiple_outputs"  "meta_is_regex_projection"  
      [189] "meta_output_name"           "meta_pop"                  
      [191] "meta_roots"                 "meta_tree_format"          
      [193] "meta_undo_aliases"          "min"                       
      [195] "mode"                       "mul"                       
      [197] "n_unique"                   "name_keep"                 
      [199] "name_map"                   "name_prefix"               
      [201] "name_prefix_fields"         "name_suffix"               
      [203] "name_suffix_fields"         "name_to_lowercase"         
      [205] "name_to_uppercase"          "nan_max"                   
      [207] "nan_min"                    "neq"                       
      [209] "neq_missing"                "new_first"                 
      [211] "new_last"                   "new_len"                   
      [213] "not"                        "null_count"                
      [215] "or"                         "over"                      
      [217] "pct_change"                 "peak_max"                  
      [219] "peak_min"                   "pow"                       
      [221] "print"                      "product"                   
      [223] "quantile"                   "rank"                      
      [225] "rechunk"                    "reinterpret"               
      [227] "rem"                        "rep"                       
      [229] "repeat_by"                  "replace"                   
      [231] "reshape"                    "reverse"                   
      [233] "rle"                        "rle_id"                    
      [235] "rolling"                    "rolling_corr"              
      [237] "rolling_cov"                "rolling_max"               
      [239] "rolling_mean"               "rolling_median"            
      [241] "rolling_min"                "rolling_quantile"          
      [243] "rolling_skew"               "rolling_std"               
      [245] "rolling_sum"                "rolling_var"               
      [247] "round"                      "sample_frac"               
      [249] "sample_n"                   "search_sorted"             
      [251] "shift"                      "shift_and_fill"            
      [253] "shrink_dtype"               "shuffle"                   
      [255] "sign"                       "sin"                       
      [257] "sinh"                       "skew"                      
      [259] "slice"                      "sort_by"                   
      [261] "sort_with"                  "std"                       
      [263] "str_base64_decode"          "str_base64_encode"         
      [265] "str_concat"                 "str_contains"              
      [267] "str_contains_any"           "str_count_matches"         
      [269] "str_ends_with"              "str_explode"               
      [271] "str_extract"                "str_extract_all"           
      [273] "str_extract_groups"         "str_find"                  
      [275] "str_hex_decode"             "str_hex_encode"            
      [277] "str_json_decode"            "str_json_path_match"       
      [279] "str_len_bytes"              "str_len_chars"             
      [281] "str_pad_end"                "str_pad_start"             
      [283] "str_replace"                "str_replace_all"           
      [285] "str_replace_many"           "str_reverse"               
      [287] "str_slice"                  "str_split"                 
      [289] "str_split_exact"            "str_splitn"                
      [291] "str_starts_with"            "str_strip_chars"           
      [293] "str_strip_chars_end"        "str_strip_chars_start"     
      [295] "str_to_date"                "str_to_datetime"           
      [297] "str_to_integer"             "str_to_lowercase"          
      [299] "str_to_time"                "str_to_titlecase"          
      [301] "str_to_uppercase"           "str_zfill"                 
      [303] "struct_field_by_name"       "struct_rename_fields"      
      [305] "sub"                        "sum"                       
      [307] "tail"                       "tan"                       
      [309] "tanh"                       "timestamp"                 
      [311] "to_physical"                "top_k"                     
      [313] "unique"                     "unique_counts"             
      [315] "unique_stable"              "upper_bound"               
      [317] "value_counts"               "var"                       
      [319] "xor"                       

# public and private methods of each class When

    Code
      ls(.pr$env[[class_name]])
    Output
      [1] "then"

---

    Code
      ls(.pr[[private_key]])
    Output
      [1] "new"  "then"

# public and private methods of each class Then

    Code
      ls(.pr$env[[class_name]])
    Output
        [1] "abs"               "add"               "agg_groups"       
        [4] "alias"             "all"               "and"              
        [7] "any"               "append"            "approx_n_unique"  
       [10] "arccos"            "arccosh"           "arcsin"           
       [13] "arcsinh"           "arctan"            "arctanh"          
       [16] "arg_max"           "arg_min"           "arg_sort"         
       [19] "arg_unique"        "arr"               "backward_fill"    
       [22] "bin"               "bottom_k"          "cast"             
       [25] "cat"               "ceil"              "clip"             
       [28] "clip_max"          "clip_min"          "cos"              
       [31] "cosh"              "count"             "cum_count"        
       [34] "cum_max"           "cum_min"           "cum_prod"         
       [37] "cum_sum"           "cumulative_eval"   "diff"             
       [40] "div"               "dot"               "drop_nans"        
       [43] "drop_nulls"        "dt"                "entropy"          
       [46] "eq"                "eq_missing"        "ewm_mean"         
       [49] "ewm_std"           "ewm_var"           "exclude"          
       [52] "exp"               "explode"           "extend_constant"  
       [55] "fill_nan"          "fill_null"         "filter"           
       [58] "first"             "flatten"           "floor"            
       [61] "floor_div"         "forward_fill"      "gather"           
       [64] "gather_every"      "gt"                "gt_eq"            
       [67] "hash"              "head"              "implode"          
       [70] "inspect"           "interpolate"       "is_between"       
       [73] "is_duplicated"     "is_finite"         "is_first_distinct"
       [76] "is_in"             "is_infinite"       "is_last_distinct" 
       [79] "is_nan"            "is_not_nan"        "is_not_null"      
       [82] "is_null"           "is_unique"         "kurtosis"         
       [85] "last"              "len"               "limit"            
       [88] "list"              "log"               "log10"            
       [91] "lower_bound"       "lt"                "lt_eq"            
       [94] "map_batches"       "map_elements"      "max"              
       [97] "mean"              "median"            "meta"             
      [100] "min"               "mod"               "mode"             
      [103] "mul"               "n_unique"          "name"             
      [106] "nan_max"           "nan_min"           "neq"              
      [109] "neq_missing"       "not"               "null_count"       
      [112] "or"                "otherwise"         "over"             
      [115] "pct_change"        "peak_max"          "peak_min"         
      [118] "pow"               "print"             "product"          
      [121] "quantile"          "rank"              "rechunk"          
      [124] "reinterpret"       "rep"               "repeat_by"        
      [127] "replace"           "reshape"           "reverse"          
      [130] "rle"               "rle_id"            "rolling"          
      [133] "rolling_max"       "rolling_mean"      "rolling_median"   
      [136] "rolling_min"       "rolling_quantile"  "rolling_skew"     
      [139] "rolling_std"       "rolling_sum"       "rolling_var"      
      [142] "round"             "sample"            "search_sorted"    
      [145] "set_sorted"        "shift"             "shift_and_fill"   
      [148] "shrink_dtype"      "shuffle"           "sign"             
      [151] "sin"               "sinh"              "skew"             
      [154] "slice"             "sort"              "sort_by"          
      [157] "sqrt"              "std"               "str"              
      [160] "struct"            "sub"               "sum"              
      [163] "tail"              "tan"               "tanh"             
      [166] "to_physical"       "to_r"              "to_series"        
      [169] "to_struct"         "top_k"             "unique"           
      [172] "unique_counts"     "upper_bound"       "value_counts"     
      [175] "var"               "when"              "xor"              

---

    Code
      ls(.pr[[private_key]])
    Output
      [1] "otherwise" "when"     

# public and private methods of each class ChainedWhen

    Code
      ls(.pr$env[[class_name]])
    Output
      [1] "then"

---

    Code
      ls(.pr[[private_key]])
    Output
      [1] "then"

# public and private methods of each class ChainedThen

    Code
      ls(.pr$env[[class_name]])
    Output
        [1] "abs"               "add"               "agg_groups"       
        [4] "alias"             "all"               "and"              
        [7] "any"               "append"            "approx_n_unique"  
       [10] "arccos"            "arccosh"           "arcsin"           
       [13] "arcsinh"           "arctan"            "arctanh"          
       [16] "arg_max"           "arg_min"           "arg_sort"         
       [19] "arg_unique"        "arr"               "backward_fill"    
       [22] "bin"               "bottom_k"          "cast"             
       [25] "cat"               "ceil"              "clip"             
       [28] "clip_max"          "clip_min"          "cos"              
       [31] "cosh"              "count"             "cum_count"        
       [34] "cum_max"           "cum_min"           "cum_prod"         
       [37] "cum_sum"           "cumulative_eval"   "diff"             
       [40] "div"               "dot"               "drop_nans"        
       [43] "drop_nulls"        "dt"                "entropy"          
       [46] "eq"                "eq_missing"        "ewm_mean"         
       [49] "ewm_std"           "ewm_var"           "exclude"          
       [52] "exp"               "explode"           "extend_constant"  
       [55] "fill_nan"          "fill_null"         "filter"           
       [58] "first"             "flatten"           "floor"            
       [61] "floor_div"         "forward_fill"      "gather"           
       [64] "gather_every"      "gt"                "gt_eq"            
       [67] "hash"              "head"              "implode"          
       [70] "inspect"           "interpolate"       "is_between"       
       [73] "is_duplicated"     "is_finite"         "is_first_distinct"
       [76] "is_in"             "is_infinite"       "is_last_distinct" 
       [79] "is_nan"            "is_not_nan"        "is_not_null"      
       [82] "is_null"           "is_unique"         "kurtosis"         
       [85] "last"              "len"               "limit"            
       [88] "list"              "log"               "log10"            
       [91] "lower_bound"       "lt"                "lt_eq"            
       [94] "map_batches"       "map_elements"      "max"              
       [97] "mean"              "median"            "meta"             
      [100] "min"               "mod"               "mode"             
      [103] "mul"               "n_unique"          "name"             
      [106] "nan_max"           "nan_min"           "neq"              
      [109] "neq_missing"       "not"               "null_count"       
      [112] "or"                "otherwise"         "over"             
      [115] "pct_change"        "peak_max"          "peak_min"         
      [118] "pow"               "print"             "product"          
      [121] "quantile"          "rank"              "rechunk"          
      [124] "reinterpret"       "rep"               "repeat_by"        
      [127] "replace"           "reshape"           "reverse"          
      [130] "rle"               "rle_id"            "rolling"          
      [133] "rolling_max"       "rolling_mean"      "rolling_median"   
      [136] "rolling_min"       "rolling_quantile"  "rolling_skew"     
      [139] "rolling_std"       "rolling_sum"       "rolling_var"      
      [142] "round"             "sample"            "search_sorted"    
      [145] "set_sorted"        "shift"             "shift_and_fill"   
      [148] "shrink_dtype"      "shuffle"           "sign"             
      [151] "sin"               "sinh"              "skew"             
      [154] "slice"             "sort"              "sort_by"          
      [157] "sqrt"              "std"               "str"              
      [160] "struct"            "sub"               "sum"              
      [163] "tail"              "tan"               "tanh"             
      [166] "to_physical"       "to_r"              "to_series"        
      [169] "to_struct"         "top_k"             "unique"           
      [172] "unique_counts"     "upper_bound"       "value_counts"     
      [175] "var"               "when"              "xor"              

---

    Code
      ls(.pr[[private_key]])
    Output
      [1] "otherwise" "when"     

# public and private methods of each class RField

    Code
      ls(.pr$env[[class_name]])
    Output
      [1] "datatype" "name"     "print"   

---

    Code
      ls(.pr[[private_key]])
    Output
      [1] "clone"            "get_datatype"     "get_name"         "new"             
      [5] "print"            "set_datatype_mut" "set_name_mut"    

# public and private methods of each class RPolarsSeries

    Code
      ls(.pr$env[[class_name]])
    Output
        [1] "abs"               "add"               "alias"            
        [4] "all"               "and"               "any"              
        [7] "append"            "approx_n_unique"   "arccos"           
       [10] "arccosh"           "arcsin"            "arcsinh"          
       [13] "arctan"            "arctanh"           "arg_max"          
       [16] "arg_min"           "arg_sort"          "arg_unique"       
       [19] "arr"               "backward_fill"     "bin"              
       [22] "bottom_k"          "cast"              "cat"              
       [25] "ceil"              "chunk_lengths"     "clear"            
       [28] "clip"              "clip_max"          "clip_min"         
       [31] "clone"             "compare"           "cos"              
       [34] "cosh"              "count"             "cum_count"        
       [37] "cum_max"           "cum_min"           "cum_prod"         
       [40] "cum_sum"           "cumulative_eval"   "diff"             
       [43] "div"               "dot"               "drop_nans"        
       [46] "drop_nulls"        "dt"                "dtype"            
       [49] "entropy"           "eq"                "eq_missing"       
       [52] "equals"            "ewm_mean"          "ewm_std"          
       [55] "ewm_var"           "exp"               "explode"          
       [58] "extend_constant"   "fill_nan"          "fill_null"        
       [61] "filter"            "first"             "flags"            
       [64] "flatten"           "floor"             "floor_div"        
       [67] "forward_fill"      "gather"            "gather_every"     
       [70] "gt"                "gt_eq"             "hash"             
       [73] "head"              "implode"           "interpolate"      
       [76] "is_between"        "is_duplicated"     "is_finite"        
       [79] "is_first_distinct" "is_in"             "is_infinite"      
       [82] "is_last_distinct"  "is_nan"            "is_not_nan"       
       [85] "is_not_null"       "is_null"           "is_numeric"       
       [88] "is_sorted"         "is_unique"         "item"             
       [91] "kurtosis"          "last"              "len"              
       [94] "limit"             "list"              "log"              
       [97] "log10"             "lower_bound"       "lt"               
      [100] "lt_eq"             "map_batches"       "map_elements"     
      [103] "max"               "mean"              "median"           
      [106] "min"               "mod"               "mode"             
      [109] "mul"               "n_chunks"          "n_unique"         
      [112] "name"              "nan_max"           "nan_min"          
      [115] "neq"               "neq_missing"       "not"              
      [118] "null_count"        "or"                "pct_change"       
      [121] "peak_max"          "peak_min"          "pow"              
      [124] "print"             "product"           "quantile"         
      [127] "rank"              "rechunk"           "reinterpret"      
      [130] "rename"            "rep"               "repeat_by"        
      [133] "replace"           "reshape"           "reverse"          
      [136] "rle"               "rle_id"            "rolling_max"      
      [139] "rolling_mean"      "rolling_median"    "rolling_min"      
      [142] "rolling_quantile"  "rolling_skew"      "rolling_std"      
      [145] "rolling_sum"       "rolling_var"       "round"            
      [148] "sample"            "search_sorted"     "set_sorted"       
      [151] "shape"             "shift"             "shift_and_fill"   
      [154] "shrink_dtype"      "shuffle"           "sign"             
      [157] "sin"               "sinh"              "skew"             
      [160] "slice"             "sort"              "sort_by"          
      [163] "sqrt"              "std"               "str"              
      [166] "struct"            "sub"               "sum"              
      [169] "tail"              "tan"               "tanh"             
      [172] "to_frame"          "to_list"           "to_lit"           
      [175] "to_physical"       "to_r"              "to_struct"        
      [178] "to_vector"         "top_k"             "unique"           
      [181] "unique_counts"     "upper_bound"       "value_counts"     
      [184] "var"               "xor"              

---

    Code
      ls(.pr[[private_key]])
    Output
       [1] "add"                         "alias"                      
       [3] "all"                         "any"                        
       [5] "append_mut"                  "arg_max"                    
       [7] "arg_min"                     "chunk_lengths"              
       [9] "clear"                       "clone"                      
      [11] "compare"                     "div"                        
      [13] "dtype"                       "equals"                     
      [15] "fast_explode_flag"           "from_arrow_array_robj"      
      [17] "from_arrow_array_stream_str" "get_fmt"                    
      [19] "is_sorted"                   "is_sorted_flag"             
      [21] "is_sorted_reverse_flag"      "len"                        
      [23] "map_elements"                "max"                        
      [25] "mean"                        "median"                     
      [27] "min"                         "mul"                        
      [29] "n_chunks"                    "n_unique"                   
      [31] "name"                        "new"                        
      [33] "panic"                       "print"                      
      [35] "rem"                         "rename_mut"                 
      [37] "rep"                         "set_sorted_mut"             
      [39] "shape"                       "sleep"                      
      [41] "sort"                        "std"                        
      [43] "struct_fields"               "sub"                        
      [45] "sum"                         "to_fmt_char"                
      [47] "to_frame"                    "to_r"                       
      [49] "value_counts"                "var"                        

# public and private methods of each class RThreadHandle

    Code
      ls(.pr$env[[class_name]])
    Output
      [1] "is_finished" "join"       

---

    Code
      ls(.pr[[private_key]])
    Output
      [1] "is_finished"        "join"               "thread_description"

# public and private methods of each class RPolarsSQLContext

    Code
      ls(.pr$env[[class_name]])
    Output
      [1] "execute"       "register"      "register_many" "tables"       
      [5] "unregister"   

---

    Code
      ls(.pr[[private_key]])
    Output
      [1] "execute"    "get_tables" "new"        "register"   "unregister"

