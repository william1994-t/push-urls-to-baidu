# push-urls-to-baidu
sitemap_txt_url="https://bashroot.top/sitemap.txt"
baidu_api="http://data.zz.baidu.com/urls?site=https://www.bashroot.top&token=64N1f4BgZ93boZV3"
 
wget $sitemap_txt_url -qO urls.txt
#curl -sL $sitemap_txt_url > urls.txt #不用wget可以改用这个
curl -s -H 'Content-Type:text/plain' --data-binary @urls.txt $baidu_api
rm -f urls.txt
