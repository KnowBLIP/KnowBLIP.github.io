# [KnowBLIP: Large Vision-Language Models meet Interleaved World Knowledge]

This is our data for the paper: 
[KnowBLIP: Large Vision-Language Models meet Interleaved World Knowledge].

## IWK-300K
1. Full single-turn conversation data is released in the following
2. The released dataset consists of the following files.
```
.
├── datasets
	--singleturn_t2t.txt: singleturn_t2t.txt includes the question, the answer,
			      the head_root image (which appear in the question)
			      and the tail_root image (which appear in the answer).
		
...   
```
```shell
[{"Q": question, "A": answer,
"head_root": image of entity in quetion,
"tail_root": image of entity in answer}]
```

## Asserts

These are our datasets analysis and template images for the paper.

## origin_images

These are original images for each entities downloaded from google, bing and yahoo. Running image_filter.py to automatically filter images.

```shell
CUDA_VISIBLE_DEVICES=0 python image_filter.py  ---image_path 'origin_image/' --top_image 10
--weight 0.2 --clip_path 'clip_14' --output_path 'img_top_10.txt'
```
