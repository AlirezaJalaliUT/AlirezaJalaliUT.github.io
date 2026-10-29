رفع خطای GitHub Pages/Jekyll: Could not locate the included file 'empty.html'

۱) پوشه zip را Extract کنید.
۲) در ریپازیتوری خود پوشه _includes را پیدا کنید.
۳) از طریق Add file -> Upload files، دو فایل داخل پوشه _includes را در مسیر _includes/ آپلود کنید.
   مهم: مسیر نهایی باید دقیقاً _includes/empty.html و _includes/publication-row.html باشد.
   اگر _includes از قبل وجود ندارد، دو فایل را از مسیر پوشه محلی _includes بکشید تا آن پوشه ساخته شود.
۴) Commit changes روی main را بزنید.
۵) تب Actions را باز کنید و نتیجه build جدید را ببینید.
۶) اگر build موفق شد، GitHub Pages سایت را منتشر می‌کند.

این بسته فقط دو include اصلی را شامل می‌شود و فایل‌های دیگر پروژه را تغییر نمی‌دهد.
