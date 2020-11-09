---
title: التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وCommon Data Service
description: يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997220"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="a6abd-103">التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="a6abd-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a6abd-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="a6abd-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="a6abd-105">على وجه التحديد، يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a6abd-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="a6abd-106">التحقق من تكوين الكتابة الثنائية في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6abd-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="a6abd-107">لتحديد ما إذا كانت الأخطاء التي تراها عند محاولة حفظ السجلات للتحديث تاتي من الكتابة الثنائية أو لا، تحقق أولاً من تكوين الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="a6abd-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="a6abd-108">إذا كانت لديك امتيازات إدارية في تطبيق Finance and Operations، فانتقل إلى **مساحات العمل\> إدارة البيانات** ، وحدد تجانب **الكتابة الثنائية**.</span><span class="sxs-lookup"><span data-stu-id="a6abd-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management** , and select the **Dual-write** tile.</span></span> <span data-ttu-id="a6abd-109">في حالة عرض تفاصيل البيئات المرتبطة وقائمة مخططات الكيانات قيد التشغيل، فإنه يتم تكوين الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="a6abd-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![التحقق من اتصال تطبيق Finance and Operationsعندما يكون لديك امتيازات المسؤول](media/verify_fin_ops_1.png)

+ <span data-ttu-id="a6abd-111">إذا لم يكن لديك امتيازات المسؤول، فستتلقى رسالة خطأ، *لا يمكن كتابة البيانات إلى كيان \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="a6abd-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="a6abd-112">في المثال الموجود في التوضيح التالي، لا يمكنك إنشاء سجل عميل في تطبيق Finance and Operations، لأنه يتم تكوين الكتابة الثنائية، ولكن لا توجد البيانات المرجعية لشروط الدفع ومجموعة العملاء في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a6abd-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![التحقق من اتصال تطبيق Finance and Operationsعندما لا يكون لديك امتيازات المسؤول](media/verify_fin_ops_2.png)

<span data-ttu-id="a6abd-114">للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في تطبيقات Finance and Operations، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="a6abd-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="a6abd-115">التحقق من تكوين الكتابة الثنائية في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a6abd-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="a6abd-116">عندما تقوم بإنشاء بيانات، إذا شاهدت حقل **الشركة** في صفحات في Common Data Service، ففنه يتم تكوين الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="a6abd-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![التحقق من اتصال Common Data Service](media/verify_cds.png)

<span data-ttu-id="a6abd-118">للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في Common Data Service، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="a6abd-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="a6abd-119">للحصول على معلومات حول كيفية عرض تفاصيل الأخطاء في حالة مصادفة أي أخطاء اثناء إنشاء البيانات في Common Data Service، راجع [تمكين وعرض تسجيل تتبع المكونات الإضافية في Common Data Service لعرض تفاصيل الأخطاء](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="a6abd-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
