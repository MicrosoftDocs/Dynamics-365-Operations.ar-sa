---
title: تكوين إعدادات البريد الإلكتروني في Microsoft Dynamics 365 Talent - Attract
description: يشرح هذا الموضوع كيفية تكوين إعدادات البريد الإلكتروني التي يتم إرسالها بواسطة Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008652"
---
# <a name="configure-email-settings"></a><span data-ttu-id="76f29-103">تكوين إعدادات البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="76f29-103">Configure email settings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="76f29-104">تعزز علامتك التجارية الثقة وتساعدك في إنشاء علاقة مع المرشحين قبل أن يتم تطبيقها للمناصب الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="76f29-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="76f29-105">يجذب التصور الإيجابي للعلامة التجارية إليك أفضل المهارات ويزيد من ولاء الموظفين الموجودين.</span><span class="sxs-lookup"><span data-stu-id="76f29-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="76f29-106">يتيح لك Microsoft Dynamics 365 Talent: Attract تكوين رسائل البريد الإلكتروني لكي تعكس العلامة التجارية لشركتك.</span><span class="sxs-lookup"><span data-stu-id="76f29-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="76f29-107">من ثم، يمكنك توفير تجربه متسقة للمرشحين للوظائف أثناء مرورهم بعملية التقديم.</span><span class="sxs-lookup"><span data-stu-id="76f29-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="76f29-108">يتيح لك تطبيق Attract تنفيذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="76f29-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="76f29-109">تكوين إعدادات البريد الإلكتروني بحيث يتم استخدام حساب خدمة البريد الإلكتروني الخاص بـ Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="76f29-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="76f29-110">بهذه الطريقة، يعرف المرشحون أن رسائل البريد الإلكتروني قادمة من شركتك.</span><span class="sxs-lookup"><span data-stu-id="76f29-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="76f29-111">على سبيل المثال، يمكنك تكوين الإعدادات بحيث يتلقى المرشحون رسائل بريد إلكتروني من `recruiting@contoso.com` بدلا من `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="76f29-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="76f29-112">قم بإنشاء علامة تجارية متسقة لجميع مراسلات البريد الإلكتروني الخاصة بك بتعيين الرأس والتذييل العموميين لقوالب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="76f29-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="76f29-113">لتكوين تطبيق Attract بحيث يستخدم حساب خدمة البريد الإلكتروني للشركة الخاصة بك لإرسال بريد إلكتروني، تحتاج إلى المكوّن الإضافي التوظيف الشامل.</span><span class="sxs-lookup"><span data-stu-id="76f29-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="76f29-114">الاتصال بحساب خدمة بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="76f29-114">Connect an email service account</span></span>

<span data-ttu-id="76f29-115">من خلال الاتصال بحساب خدمة البريد الإلكتروني للشركة الخاصة بك، يمكنك إنشاء تجربة بريد إلكتروني خاصة بالعلامة التجارية للمرشحين للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="76f29-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="76f29-116">إذا لم تقم بتوصيل حساب الشركة الخاص بك، عندئذ يستخدم Attract حساب خدمة البريد الإلكتروني الذي يحمل العلامة التجارية الافتراضية لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="76f29-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="76f29-117">حدد **الإعدادات** (رمز الترس في الزاوية العلوية اليمنى)، ثم حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="76f29-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="76f29-118">في علامة تبويب **إعدادات البريد الإلكتروني**، تحت  **حسابات خدمه البريد الإلكتروني**، حدد **الاتصال بحساب الشركة**.</span><span class="sxs-lookup"><span data-stu-id="76f29-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![الاتصال بحساب خدمة البريد الإلكتروني للشركة في Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="76f29-120">لمزيد من المعلومات حول كيفية إنشاء حساب بريد إلكتروني مشترك، راجع [علب البريد الإلكتروني المشتركة في  Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="76f29-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="76f29-121">في إطار تسجيل الدخول إلى Microsoft، قم بتسجيل الدخول باستخدام بيانات الاعتماد الخاصة بشركك.</span><span class="sxs-lookup"><span data-stu-id="76f29-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="76f29-122">إذا لم تكن قد قمت بعد بإعداد حساب خدمة بريد إلكتروني، أو إذا كنت ترغب في إضافة خدمة جديدة، فحدد **حدد إضافة حساب خدمة جديد**، ثم أدخل معلومات البريد الإلكتروني الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="76f29-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="76f29-123">إذا كنت قد قمت بالفعل بإعداد حساب خدمة بريد إلكتروني ترغب في استخدامه، فقم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="76f29-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="76f29-124">عند تكوين حساب خدمة البريد الإلكتروني بنجاح، ستشاهده مدرجا تحت **حسابات خدمة البريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="76f29-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="76f29-125">فصل الاتصال بحساب خدمة بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="76f29-125">Disconnect an email service account</span></span>

<span data-ttu-id="76f29-126">إذا أردت التوقف عن استخدام مجال الشركة في اتصالات البريد الإلكتروني من خلال Attract، فيمكنك قطع اتصال حساب خدمة البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="76f29-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="76f29-127">حدد **الإعدادات** (رمز الترس في الزاوية العلوية اليمنى)، ثم حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="76f29-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="76f29-128">في علامة تبويب **إعدادات البريد الإلكتروني**، تحت **حسابات خدمة البريد الإلكتروني**، حدد زر **المزيد**  (ثلاثة نقاط عمودية) بجانب حساب خدمة البريد الإلكتروني الذي تريد قطع الاتصال به.</span><span class="sxs-lookup"><span data-stu-id="76f29-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="76f29-129">حدد **قطع اتصال بحساب البريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="76f29-129">Select **Disconnect email account**.</span></span>

    ![قطع الاتصال بحساب خدمة البريد الإلكتروني لشركتك](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="76f29-131">عند مطالبتك بتأكيد العملية، حدد **قطع الاتصال.**</span><span class="sxs-lookup"><span data-stu-id="76f29-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![تأكيد قطع الاتصال بحساب خدمة البريد الإلكتروني لشركتك](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="76f29-133">إذا لم تقم بالاتصال بحساب خدمة بريد إلكتروني مختلف، ستستخدم رسائل البريد الإلكتروني التي يتم إرسالها من Attract حساب خدمة البريد الإلكتروني الافتراضي الذي يحمل علامة Microsoft التجارية.</span><span class="sxs-lookup"><span data-stu-id="76f29-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="76f29-134">تكوين إعدادات قالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="76f29-134">Configure email template settings</span></span>

<span data-ttu-id="76f29-135">يمكنك تحميل صوره لشعار الشركة ومعلومات أخرى كرأس يحمل العلامة التجارية في رسائل البريد الإلكتروني الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="76f29-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="76f29-136">يمكنك أيضا توفير ارتباطات إلى نهج الخصوصية الخاص بك وشروط الاستخدام في تذييلات البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="76f29-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="76f29-137">ويجب عليك التزام بكافة قوانين البلد أو المنطقة المعمول بها، وكذلك البلد أو المنطقة التي تحكم مستلم البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="76f29-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="76f29-138">تتضمن هذه القوانين لوائح مكافحة البريد الإلكتروني العشوائي.</span><span class="sxs-lookup"><span data-stu-id="76f29-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="76f29-139">حدد **الإعدادات** (رمز الترس في الزاوية العلوية اليمنى)، ثم حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="76f29-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="76f29-140">في علامة تبويب **إعدادات البريد الإلكتروني**، تحت **إعدادات قالب البريد الإلكتروني**، اسحب الصورة التي تريد استخدامها كرأس للبريد الإلكتروني الخاص بك في مربع الصورة، أو انقر فوق مربع الصورة لاستعراض ملف.</span><span class="sxs-lookup"><span data-stu-id="76f29-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="76f29-141">لاستبدال صورة موجودة، يجب أولا تحديد **إزالة** بجوارها.</span><span class="sxs-lookup"><span data-stu-id="76f29-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="76f29-142">يجب أن تكون الصورة ملف JPEG أو JPG أو PNG أو SVG.</span><span class="sxs-lookup"><span data-stu-id="76f29-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="76f29-143">الحجم الموصي به للصور بين 25 و 800 بكسل للعرض، وبين 25 و 150 بكسل للارتفاع.</span><span class="sxs-lookup"><span data-stu-id="76f29-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="76f29-144">الحد الأقصى لحجم الملف للرأس هو 1 ميغابايت (MB).</span><span class="sxs-lookup"><span data-stu-id="76f29-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![إضافة صورة لرأس البريد الإلكتروني لشركتك](./media/attract-admin-email-header.png)

3. <span data-ttu-id="76f29-146">تحت **سياسة الخصوصية لمراسلاتك**، قم بتوفير ارتباط إلى سياسة الخصوصية الخاصة بشركك.</span><span class="sxs-lookup"><span data-stu-id="76f29-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="76f29-147">تحت **شروط وأحكام المراسلات**، قم بتوفير ارتباط لشروط الاستخدام في شركتك.</span><span class="sxs-lookup"><span data-stu-id="76f29-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![إضافة ارتباطات إلى سياسة الخصوصية وشروط الاستخدام الخاصة بالشركة في تذييل البريد الإلكتروني](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="76f29-149">حدد **حفظ** لحفظ إعدادات قوالب البريد الإلكتروني الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="76f29-149">Select **Save** to save your email template settings.</span></span>
